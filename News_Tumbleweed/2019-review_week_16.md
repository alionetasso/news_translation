Nouvelles de Tumbleweed en semaine 16/2019: mise à jour de Curl, Salt et de la suite FFmpeg
===========================================================================================

Trois clichés openSUSE Tumbleweed de qualité ont été publiés depuis jeudi dernier avec des paquets mis à jour pour Curl, Salt, FFmpeg et plus.

**Mozilla Firefox** a publié une version mineure de la version 66.0.3 dans le dernier instantané Tumbleweed 20190415. Le navigateur a résolu certains problèmes de performances avec certains jeux HTML5 et fourni un plug-in de recherche Baidu destiné aux utilisateurs chinois et à l’espace Internet chinois.
**Curl 7.64.1**, l'outil de ligne de commande permettant de transférer des données à l'aide de divers protocoles, a corrigé de nombreux bogues et ajouté des bibliothèques supplémentaires pour vérifier la prise en charge du protocole LDAP (*Lightweight Directory Access Protocol*).
La mise à jour de **libvirt 5.2.0** a supprimé quelques correctifs et ajouté plusieurs nouvelles fonctionnalités, telles que les capacités de pool de stockage, pour obtenir une liste de sortie XML plus détaillée pour l'interface de programmation d'application (API) *virConnectGetStoragePoolCapabilites*. **Libvirt** a également activé la sélection automatique du microprogramme pour l'émulateur open source QEMU.
Le tout nouveau paquet **salt 2019.2.0** de Tumbleweed a amélioré l'automatisation du réseau et étendu la prise en charge de divers systèmes d'exploitation via le réseau, ainsi que de fonctionnalités de manipulation de la configuration ou d'exécution de commandes opérationnelles. **Salt** a également ajouté l'exécution de *playbooks* à la version 2019.2.0 avec la fonction `playbooks`et inclut un module pour les `states` *ansible*, qui peut être utilisé sur un hôte ciblé pour exécuter des *playbooks*, ou utilisé dans un orchestrateur de `states`.
Selon l'évaluateur de Tumbleweed, l’instantané avait une cote de 95 au moment de la publication de cet article.

Le cliché 20190412 a obtenu une note de 94 et a apporté une mise à jour à **Ceph** qui a ajouté une option distincte permettant de configurer un port SSL (*Secure Sockets Layer*).
Le paquet **cifs-utils 6.9**, qui fait partie du projet Samba, a ajouté des correctifs pour Azure et supprimé plusieurs bogues.
Le paquet **libssh2_org 1.8.2** a rectifié un correctif mal appliqué qui cassait sa version précédente.
Quelques paquets **YaST** comportaient des mises à jour, comme le paquet **yast2-storage-ng 4.2.5**, qui permet un nouveau format pour importer/exporter des lecteurs NFS (*Network File System*).

L’instantané 20190411 a démarré la semaine et affichait un score modérément stable de 89. Cet instantané apportait le noyau **Linux 5.0.7** et offrait un potentiel d’atténuation pour un appel système **ptrace** pour PowerPC.
Il y avait quelques corrections de bugs pour les codecs, les filtres et les formats dans la mise à jour 4.1.3 de **ffmpeg**.
Le connecteur JavaScript pour GNOME, **gjs 1.56.0**, contenaient des modifications très importantes par rapport à la version précédente 1.54.3 de Tumbleweed. Les *changelog* précédents ont identifié un bogue GNU Compiler Collection 9 et ajouté des règles ESLint. La nouvelle version était une version stable.
Le paquet **python-kiwi 9.17.35** a corrigé les régressions pour le module **kiwi-repart dracut**.
Le package **wget 1.20.3** a corrigé la vulnérabilité de débordement de la mémoire tampon trouvée dans le Common Vulnerabilities and Exposures (*CVE*) 2019-5953.
L’éditeur de texte **vim 8.1.1137** a corrigé plusieurs bogues, dont un test Python qui n’effaçait pas le tampon caché et une espace dans la colonne de numérotation de ligne qui se trouvait du mauvais côté lorsque le paramètre *rightleft* était activé.
