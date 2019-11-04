Aller plus loin avec Btrfs dans YaST
------------------------------------

19 juin 2019 par [Yast Team](https://lizards.opensuse.org/author/yast-team/ "Posts de Yast Team")

Depuis que l'équipe YaST a réécrit la pile de logiciels pour la gestion des périphériques de stockage, nous avons régulièrement ajouté et présenté de nouvelles fonctionnalités dans ce domaine. Cela inclut, entre autres caractéristiques, la [capacité de formater et de partitionner](http://yast.opensuse.org/blog/2018/10/09/highlights-of-yast-development-sprint-64/#changes- in-the-partitioner-ui-to-leash-the-storage-ng-power) tout type de périphériques et la possibilité de [créer et gérer des périphériques Bcache](https://lizards.opensuse.org/2019/02/27/recap-bcache-in-yast/). Le moment est venu de présenter une autre fonctionnalité très attendue qui vient d'arriver dans openSUSE Tumbleweed: la prise en charge des systèmes de fichiers Btrfs à plusieurs périphériques.

Comme nos lecteurs habituels le savent sûrement, Btrfs est un système de fichiers moderne pour Linux destiné à implémenter des fonctionnalités avancées qui vont au-delà de la portée et des capacités des systèmes de fichiers traditionnels. Ces capacités incluent des sous-volumes (racines de système de fichiers internes distinctes), des instantanés inscriptibles et en lecture seule, une sauvegarde incrémentielle efficace et notre spécialité actuelle: prise en charge de la distribution d'un système de fichiers unique sur plusieurs périphériques en mode bloc.

### Btrfs multi-périphériques en un coup d’œil

YaST prend désormais en charge le système de fichiers multi-périphérique Btrfs ... mais qu'est-ce que cela signifie exactement? Aussi simple que cela puisse paraître, il est possible de créer un système de fichiers Btrfs sur plusieurs disques, partitions ou tout autre périphérique en mode bloc. Un peu comme un RAID défini par logiciel. En fait, vous pouvez l'utiliser pour remplacer complètement les RAID logiciels.

Voyons un exemple. Imaginez que vous avez deux disques, `/dev/sda` et`/dev/sdb`, et que vous avez également des partitions sur le premier disque. Vous pouvez créer un système de fichiers Btrfs en même temps sur certains périphériques, par exemple, sur `/dev/sda2` et`/dev/sdb`, de sorte que vous disposerez d'une configuration ressemblant à ceci.

            /dev/sda                /dev/sdb
                |                       |   
                |                       |   
         ---------------                |   
        |               |               |   
        |               |               |   
    /dev/sda1       /dev/sda2           |   
                        |               |   
                        |               |   
                         ---------------
                                |   
                              Btrfs
                                |   
                                |   
                                @ (default subvolume)
                                |   
                                |   
                     -----------------------
                    |       |       |       |   
                    |       |       |       |   
                  @/home  @/log   @/srv    ...

Une fois que le système de fichiers est installé sur plusieurs périphériques, vous pouvez le configurer pour effectuer le fractionnement de données, la mise en miroir, le traçage + miroir, etc. En gros, tout ce que le RAID peut faire. En fait, vous pouvez configurer comment traiter les données et les méta-données Btrfs séparément. Par exemple, vous pouvez décider de faire un striping avec vos données (en définissant le niveau RAID de données sur la valeur `raid0`) et de faire une mise en miroir avec les méta-données Btrfs (en le définissant au niveau` raid1`). Pour les données et les méta-données, vous pouvez utiliser les niveaux suivants: `single`,` dup`, `raid0`,` raid1`, `raid10`,` raid5` et `raid6`.

La combinaison de cette fonctionnalité et des sous-volumes Btrfs ouvre un monde presque infini de possibilités. En gros, il vous permet de gérer l’ensemble de votre configuration de stockage à partir du système de fichiers lui-même. L'utilisation d'outils et de couches distinctes, tels que les logiciels RAID ou LVM définis par logiciel, est tout simplement inutile si vous utilisez Btrfs dans toute sa splendeur.

### Gestion de Btrfs multi-périphériques avec le partitionneur YaST

Caractéristique intéressante, mais par où commencer? Comme d'habitude, YaST vous apporte la réponse! Voyons comment la version de YaST actuellement intégrée à openSUSE Tumbleweed facilitera la gestion de cette fonctionnalité intéressante de Btrfs. Les utilisateurs de SLE et de Leap devront attendre la prochaine version (15.2) pour profiter pleinement de toutes les fonctionnalités.

Tout d’abord, la section Btrfs de notre cher partitionneur Expert a été réaménagée comme indiqué dans l’illustration suivante.

![Nouvelle section Btrfs du partitionneur](https://lizards.opensuse.org/wp-content/uploads/2019/06/btrfs_section-300x157.png)

Il répertorie tous les systèmes de fichiers Btrfs, mono et multi-périphériques. Vous pouvez les distinguer au premier abord par le format du nom. La table contient les informations les plus pertinentes sur les systèmes de fichiers, ainsi que des boutons pour ajouter un nouveau système de fichiers et pour supprimer et modifier les systèmes existants.

Le système de fichiers Btrfs existant peut être inspecté et modifié de plusieurs manières. L'onglet "Présentation" comprend des détails tels que le point de montage, l'étiquette du système de fichiers, l'UUID, les niveaux RAID de données et de métadonnées, etc. Le système de fichiers peut être modifié pour changer certains aspects tels que les options de montage ou les sous-volumes.

![Vue d'ensemble d'un système de fichiers Btrfs](https://lizards.opensuse.org/wp-content/uploads/2019/06/show-300x157.png)

De plus, l'onglet "Périphériques utilisés" contient une liste détaillée des périphériques bloqués utilisés par le système de fichiers. Cette liste peut également être modifiée pour ajouter ou supprimer des périphériques. Notez qu'une telle opération ne peut être effectuée que lorsque le système de fichiers n'existe pas encore sur le disque. Théoriquement, Btrfs permet d'ajouter et de supprimer des périphériques d'un système de fichiers déjà créé, mais une opération d'équilibrage serait nécessaire par la suite. Une telle opération d'équilibrage pourrait prendre un temps considérable, pour cette raison, elle a été évitée dans le partitionneur expert.

![Périphériques d'un système de fichiers Btrfs](https://lizards.opensuse.org/wp-content/uploads/2019/06/used_devices-300x158.png)

Bien sûr, vous pouvez toujours formater un seul périphérique en tant que Btrfs de manière traditionnelle (en utilisant le bouton "edit" pour un tel périphérique). Mais voyons comment le nouveau bouton d’ajout d’un système de fichiers Btrfs ouvre de nouvelles possibilités.

![Ajout d'un système de fichiers Btrfs](https://lizards.opensuse.org/wp-content/uploads/2019/06/add_filesystem-300x157.png)

Semblable à la boîte de dialogue RAID, vous avez les périphériques disponibles à gauche et vous pouvez sélectionner les périphériques sur lesquels vous souhaitez créer le système de fichiers. Vous pouvez également indiquer les niveaux RAID de données et de méta-données. Bien entendu, les niveaux RAID admissibles dépendront du nombre de périphériques sélectionnés. Vous passerez à la deuxième étape de la création de Btrfs en cliquant sur le bouton "Suivant". Dans cette deuxième étape, vous pouvez sélectionner les options de montage et définir les sous-volumes, voir l'image suivante.

![Options pour un nouveau système de fichiers Btrfs](https://lizards.opensuse.org/wp-content/uploads/2019/06/options-300x203.png)

Et en plus de tout cela, le partitionneur expert a reçu plusieurs petites améliorations après l’inclusion de systèmes de fichiers Btrfs à plusieurs périphériques. Maintenant que les systèmes de fichiers multi-périphériques Btrfs sont considérés comme des citoyens de première classe, ils sont inclus dans la liste générale des périphériques. Notez que la colonne "Type" a également été améliorée pour afficher des informations plus utiles, non seulement pour Btrfs mais pour tous les types de périphériques.

![Liste modifiée de périphériques](https://lizards.opensuse.org/wp-content/uploads/2019/06/devices_list-300x157.png)

### Quoi d'autre fonctionne?

Mais YaST va bien au-delà du partitionneur. Nous nous sommes également assurés que la proposition de stockage (c'est-à-dire la configuration guidée) peut prendre en charge les configurations Btrfs multi-périphériques existantes lorsque vous effectuez une nouvelle installation. De plus, le processus de mise à niveau est également prêt à fonctionner avec votre système de fichiers Btrfs à plusieurs périphériques.

Enfin, AutoYaST peut également être utilisé pour spécifier ce type de configuration Btrfs. La [documentation officielle d'AutoYaST](https://www.suse.com/documentation/sles-15/singlehtml/book_autoyast/book_autoyast.html) comprendra une section spécifique sur la gestion avancée des systèmes de fichiers Btrfs au-dessus de plusieurs périphériques en mode bloc. Le contenu est en cours de révision par l'équipe de documentation de SUSE.

### Qu'est-ce qui ne fonctionne pas (encore)?

Il y a toujours un scénario qui n'est pas couvert à 100%. Comme décrit dans [bug\#1137997](https://bugzilla.suse.com/show_bug.cgi?id=1137997), il n’est toujours pas possible d’utiliser le bouton "Importer les points de montage" dans le partitionneur pour recréer une structure multi-périphériques Btrfs. Mais ne craignez rien, c'est dans notre liste de choses à réparer à court terme!

### Testez-le dès qu'il sort du four!

Le développement de logiciels libres est un processus collaboratif et nous avons maintenant besoin de VOUS pour faire votre part. Veuillez tester cette nouvelle fonctionnalité et signaler les bogues si quelque chose ne fonctionne pas comme prévu. Et s'il vous plait, venez avec vos idées et autres améliorations et cas d'utilisation. Et bien sûr, *Have a lot of fun!*
