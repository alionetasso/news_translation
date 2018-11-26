Le temps passe vite et un autre sprint de développement est terminé pour l'équipe YaST. Au cours de celle-ci, nous nous sommes concentrés sur l'amélioration du processus d'installation, son affinement et l'ajout de nouvelles fonctionnalités afin de libérer de nouvelles possibilités. Qui comprend:

    Plus d'options pour configurer Kubic lors de l'installation.
    Plusieurs améliorations dans la proposition de stockage.
    Faciliter la configuration du réseau et l'utilisation des référentiels en ligne dans openSUSE.
    Amélioration de l’installation en mode texte pour CJK et d’autres langues.
    Configuration de l'accès SSH lors de l'installation et dans un système en cours d'exécution.
    Et beaucoup d'autres petites corrections ici et là!

    Nombre de ces fonctionnalités seront déjà disponibles dans openSUSE Tumbleweed en novembre (le sprint vient juste de se terminer le 16 novembre et le processus d'intégration prend généralement quelques jours), d'autres seront visibles pour la première fois dans les prochains SLE-15-SP1 et Leap 15.1 Alpha. versions.
    Nouveaux dialogues dans l'installation openSUSE Kubic

    Les produits SUSE CaaSP et openSUSE Kubic ont reçu un nouveau flux de travail d'installation il y a quelque temps. A l'origine, ils utilisaient un workflow d'installation spécifique (une seule boîte de dialogue de configuration tout-en-un), mais le problème était que de nombreuses fonctionnalités d'installation openSUSE / SLE étaient manquantes car le code du programme d'installation était complètement différent.

    Cela a été changé il y a quelque temps pour utiliser l'installation habituelle comme dans les produits standard SLE ou openSUSE. Vous pouvez lire les détails du nouveau processus d'installation sur la page wiki de Kubic.

    Cependant, les produits CaaSP ou Kubic nécessitaient des paramètres plus spécifiques en fonction du rôle sélectionné. Pendant ce sprint, nous avons ajouté les étapes correspondantes à l’installation.

    Nouvelles étapes d'installation pour openSUSE Kubic

    Actuellement, la boîte de dialogue supplémentaire ne demande que l'adresse du serveur NTP, mais d'autres options peuvent être ajoutées ultérieurement.
    Amélioration de la prise en charge du mode texte pour CJK et d’autres langues

    YaST est capable de gérer de nombreuses langues, même en mode texte. Lorsqu'un utilisateur souhaite exécuter le programme d'installation en mode texte dans certaines langues, telles que le chinois, le japonais ou le coréen, YaST utilise un émulateur de terminal spécial appelé fbiterm, capable d'afficher les caractères nécessaires à ces langues.

    Désormais, au lieu de conserver deux approches différentes en fonction de la langue, YaST tentera d'utiliser cet émulateur de terminal spécial chaque fois que cela est possible pour toutes les installations basées sur du texte. Malheureusement, il existe un petit ensemble de langues qui ne sont pas correctement gérées par fbiterm. Dans ces cas, YaST informera l'utilisateur du problème et celui-ci retombera en anglais.

    YaST installe SLE-15-SP1 en japonais

    Suite à cette unification, la police utilisée lors de l’installation du mode texte a changé pour toutes les langues qui n’utilisaient pas fbiterm auparavant. Il est donc possible que votre installation de SUSE ou d'openSUSE soit légèrement différente.
    Proposition de stockage: jouer avec la technologie Intel Rapid Start

    La technologie Intel Rapid Start (également appelée IRST) permet aux systèmes de reprendre rapidement leur activité en veille profonde (par exemple, si votre batterie s'épuise) C’est une technologie pilotée par un microprogramme qui repose sur l’existence d’une partition spéciale située sur un SSD (Solid State Device).

    Mais notre proposition de partitionnement (la soi-disant configuration guidée) n'était pas consciente du rôle important de cette partition. Il a donc parfois été suggéré de la supprimer afin d'utiliser l'espace libéré pour l'installation de SUSE (ouvert) par dessus.

    Nous l'avons amélioré et la partition IRST ne sera supprimée qu'en dernier recours, si la suppression de toutes les autres partitions autorisées sur le disque n'est toujours pas suffisante pour adapter le nouveau système. De plus, une partition IRST située sur le même disque qu'un système Windows ne sera supprimée que si l'utilisateur autorise explicitement la proposition de stockage à supprimer cette installation Windows.
    Exécution de la proposition de stockage sur des RAID logiciels et des périphériques USB

    Mais ce n’est pas la seule amélioration apportée dans le domaine de la configuration guidée du partitionnement. Nous avons également élargi son utilité en lui permettant d'être utilisé sur de nouveaux types d'appareils.

    Tout d’abord, il est maintenant possible d’exécuter la configuration guidée sur un logiciel MD RAID. Pour cela, les RAIDs candidats doivent remplir l'une des deux conditions suivantes: contenir une table de partition ou être complètement vide (ce qui implique de ne pas être formaté, chiffré ou utilisé à d'autres fins). C’est non seulement une autre étape pour tirer parti de la capacité relativement récente de YaST à partitionner des RAID logiciels (grâce à libstorage-ng), mais également un moyen très naturel de prendre en charge l’utilisation des contrôleurs RAID EMC PowerEdge Dell S130 et S140, qui offrent une solution hybride basée sur des RAID logiciels mais sauvegardée par une configuration pilotée par un microprogramme.

    Proposition de partitionnement sur un logiciel MD RAID

    À peu près au même prix, nous avons décidé qu'il était temps d'offrir les périphériques USB disponibles en tant que candidats à la configuration guidée, même s'il existe également des candidats non USB. À l’exclusion, bien sûr, du support d’installation (sauf lorsqu’un réseau est exécuté).
