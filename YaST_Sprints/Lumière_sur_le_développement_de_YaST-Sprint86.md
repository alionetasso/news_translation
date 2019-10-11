Maintenant que vous avez eu l'occasion de consulter [notre message sur les options de chiffrement avancées](https://lizards.opensuse.org/2019/10/09/advanced-encryption-yast/) (en particulier si vous êtes un utilisateur de s390), il est temps de vérifier ce qui s’est passé lors du dernier sprint de développement YaST, qui s’est achevé lundi dernier.

Comme d'habitude, nous avons travaillé sur un large éventail de sujets, notamment:

- Amélioration de la prise en charge des systèmes de fichiers multi-périphériques dans le partitionneur expert.
- Résolution des problèmes de réseau, de démarrage sécurisé et de kdump dans AutoYaST.
- Plus d'attente de `chrony` lors du démarrage initial lorsque cela n'a pas de sens.
- Préparation de la prise en charge de la scission des fichiers de configuration entre `/usr/etc` et` /etc`.
- Utilisation de `/etc/sysctl.d` pour écrire les paramètres liés à YaST au lieu du fichier principal `/etc/sysctl.conf`.

### Expert Partitioner et systèmes de fichiers multi-périphériques

Jusqu'à présent, le partitionnement en mode expert partait du principe que Btrfs était le seul système de fichiers construit sur plusieurs périphériques. Mais ce n'est pas tout à fait vrai, car certains systèmes de fichiers peuvent utiliser un journal externe pour améliorer les performances. Par exemple, *Ext3/4* et *XFS* peuvent être configurés pour utiliser des périphériques distincts pour les données et la journalisation.

Nous avons reçu un [rapport de bogue](https://bugzilla.suse.com/show_bug.cgi?id=1145841) causé par ce malentendu sur les systèmes de fichiers multi-périphériques. Le partitionneur expert désignait comme "faisant partie de Btrfs" un périphérique utilisé comme journal externe d'un système de fichiers *Ext4*. Nous avons donc amélioré cette fonctionnalité lors du dernier sprint et les périphériques de journal externes sont maintenant correctement indiqués dans la colonne *Type* du Partitionneur expert, comme illustré dans la capture d'écran ci-dessous.

![Type de journal externe](http://lizards.opensuse.org/wp-content/uploads/2019/10/yast2-storage-ng-type-for-external-journal-devices-300x225.png)

De plus, les informations sur le système de fichiers indiquent maintenant quel périphérique est utilisé pour le journal externe.

![Détails du périphérique de journal externe](http://lizards.opensuse.org/wp-content/uploads/2019/10/yast2-storage-ng-external-journal-device-details-300x225.png)

Enfin, nous avons également limité l’utilisation des périphériques appartenant à un système Btrfs multi-périphériques. À présent, vous recevrez un message d'erreur si vous essayez de modifier l'un de ces périphériques. À l'avenir, nous étendrons cette fonctionnalité pour permettre de modifier les systèmes de fichiers utilisant un journal externe via le Partitionneur expert.

### AutoYaST a fait l'objet de notre attention

Au cours de ce sprint, nous avons accordé à AutoYaST une attention particulière dans différents domaines: réseaux, chargeur de démarrage et kdump.

À propos de la zone réseau, nous avons terminé la prise en charge de s390 dans la nouvelle couche réseau, en corrigeant certaines anciennes limitations en matière d’activation de périphériques et de gestion d’UDev. En dehors de cela, nous avons corrigé plusieurs bugs et amélioré beaucoup la documentation, car nous la trouvions plutôt incomplète.

Un autre changement important a été l'ajout de la possibilité de désactiver le démarrage sécurisé pour UEFI via AutoYaST. Bien sûr, nous avons également mis à jour la documentation et, au cours du processus, nous avons ajouté des éléments manquants et supprimé d'autres éléments inutiles.

Enfin, nous avons corrigé un problème délicat lorsque nous essayons de faire fonctionner kdump sur un système minimal. Après débogage, nous avons découvert qu’AutoYaST ajoutait trop tard `kdump` à la liste des paquets à installer. Ce problème a été résolu et il devrait maintenant fonctionner comme un charme.

Comme vous l'avez peut-être vu, à part l'écriture de code, nous essayons de contribuer à la documentation afin que nos utilisateurs disposent d'une bonne source d'informations. Si vous êtes curieux, en plus des documents pour les versions [SUSE](https://suse.com/documentation) et [openSUSE](https://doc.opensuse.org/) publiées, vous pouvez consulter les [dernières versions](https://susedoc.github.io/) (y compris le [manuel AutoYaST](https://susedoc.github.io/doc-sle/master/SLES-autoyast/html)). Félicitations à notre équipe de documentation pour cet extraordinaire travail !

### Éviter le temps mort `chrony-wait`

Récemment, certains utilisateurs d’openSUSE ont signalé un problème très gênant dans Tumbleweed. Lorsque la synchronisation de l'heure est activée via YaST, le système peut rester bloqué pendant le processus de démarrage si aucune connexion réseau n'est disponible.

Le problème est que, mis à part le service `chrony`, YaST activait également le service` chrony-wait`. Ce service est utilisé pour garantir que l'heure est correctement définie avant de continuer avec d'autres services pouvant être affectés par un décalage temporel. Mais sans connexion réseau, `chrony-wait` attendra environ 10 minutes. Inacceptable.

La discussion sur le correctif de ce bogue est toujours ouverte, mais pour le moment, nous avons appliqué une solution de contournement dans YaST afin d'activer `chrony-wait` uniquement pour les produits nécessitant une heure précise, comme openSUSE Kubic. Dans le reste des cas, les systèmes démarreront plus rapidement, même sans réseau, bien que certains services puissent être affectés par un décalage temporel.

### Fractionnement des fichiers de configuration entre `/etc` et `/usr/etc`

En tant qu'utilisateurs Linux, nous sommes tous habitués à vérifier les paramètres du système dans `/etc`, qui contient un mélange de valeurs de configuration propres au fournisseur et à l'hôte. Cette approche a plutôt bien fonctionné dans le passé, non sans quelques ratés, mais lorsque des choses comme [les mises à jour transactionnelles](https://en.opensuse.org/openSUSE:Packaging_for_transactional-updates) entrent en jeu, la situation devient compliquée.

Afin de résoudre ces problèmes, il est prévu de scinder les fichiers de configuration entre `/etc` et `/usr/etc`. Le premier contiendrait les paramètres du fournisseur, tandis que le second définirait des valeurs spécifiques à l'hôte. Bien sûr, une telle démarche a de nombreuses implications.

Au cours de ce sprint, nous avons donc essayé d'identifier les problèmes potentiels pour YaST et de proposer des solutions pour les résoudre à l'avenir. Si vous êtes intéressé par les détails techniques, vous pouvez lire [nos conclusions](https://github.com/yast/yast-yast2/blob/2975c70ab17f1bc790c0ca3e77ff7a0d14a08266/doc/etc-et-usr-etr-etc.md).

### Écrire les modifications de Sysctl  dans `/etc/sysctl.d`

Pour pouvoir gérer la séparation de `/etc` et `/usr/etc`, YaST doit arrêter d’écrire dans des fichiers tels que `/etc/sysctl.conf` et utiliser un fichier spécifique dans les répertoires `.d` (comme `/etc/sysctl.d`).

Ainsi, dans le cadre de la recherche susmentionnée, nous avons adapté plusieurs modules (`yast2-network`,` yast2-tune`, `yast2-security` et` yast2-vpn`) afin qu'ils se comportent de cette manière concernant `/etc/sysctl.conf`. À partir de maintenant, les paramètres spécifiques à YaST seront écrits dans `/etc/sysctl.d/30-yast.conf` au lieu de `/etc/sysctl.conf`. De plus, si YaST trouve l'un de ces paramètres dans le fichier `.conf` général, il les déplacera au nouvel emplacement.

### Et après?

Sprint 87 est déjà en cours. Outre la correction de certains bugs introduits lors de la refactorisation du réseau, nous prévoyons de travailler sur d'autres tâches liées au stockage, telles que le support du redimensionnement pour LUKS2 ou certains problèmes liés a snapper. Nous vous donnerons plus de détails dans notre prochain rapport de sprint.

Restez à l'écoute!
