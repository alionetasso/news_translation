Tumbleweed commence l'année avec KDE Plasma et KDE Applications, VIM et curl
=============================================================================
*18 janvier 2019 par Douglas DeMaio*

Cette nouvelle année a commencé avec la mise à jour de plusieurs paquets pour les utilisateurs de Tumbleweed.

Jusqu'à présent, trois instantanés ont été publiés en 2019 et parmi les paquets mis à jour, citons Plasma, VIM, RE2, QEMU et curl.

L'instantané 20190112 a apporté bon nombre de nouveautés. La nouvelle version *Long Terme Release* de **nodejs10 10.15.0** corrigeait certaines vulnérabilités de synchronisation, mettait à jour une dépendance avec une mise à niveau vers **OpenSSL 1.1.0j** et la version contenait également une configuration du délai d'expiration de 40 secondes qui est maintenant appliqué aux serveurs recevant des en-têtes HTTP.
Le journal des modifications de **Vim** liste plusieurs correctifs pour cette éditeur de texte hautement configurable avec la version **8.1.0687**, qui devrait maintenant pouvoir être construite avec **Ruby 2.6.0**, publié fin décembre.
Google **re2 20190101** apporte quelques modifications de performances et des corrections de bugs.
L'algorithme de compression rapide en temps réel de **zstd 1.3.8** offre une meilleure vitesse de décompression pour les fichiers volumineux.
Le paquet **yast2-firewall**, introduit dans l’instantané 20190110, a été modifié pour permettre l’insertion de nouveaux éléments *«forward_ports», «rich_rules»* et *«source_ports»* dans les entrées de zone avec **yast2-schema 4.1.0**.

**KDE Plasma 5.14.5** est arrivé en instantané 20190110; la mise à jour a corrigé la limite de cache maximale pour les addons Plasma.
Des mises à jour ont également été mises à jour pour Breeze GTK, Discover, KWin, Plasma Workspace, Powerdevil, etc.
**powertop 2.10**, l'outil Intel qui fournit des modes d'économie d'énergie en espace utilisateur, pour le noyau et le matériel, prend en charge le support d'Intel GLK, anciennement Gemini Lake, et le support d'Intel CNL-U/Y.
Le paquet de services de géolocalisation **geoclue2 2.5.2** comportait une modification qui autorisait plusieurs clients sur la même connexion D-Bus et ajoutait une interface de programmation d'application (API) pour celle-ci, ce qui était principalement fait pour le portail de localisation Flatpak.
Le client IRC **irssi 1.1.2** avait plusieurs correctifs et synchronisait un nouveau script.
**Jhbuild 3.28.0** de GNOME a permis de compiler des tests de libosinfo. Les traductions ont été mises à jour pour le tchèque avec **libstorage-ng 4.1.75** via Weblate et plusieurs packages YaST ont été mis à jour, notamment **yast2 4.1.48** et **yast2-multipath 4.1.1**, qui permettaient de résoudre le problème de l’utilisation d’un nom de fichier aléatoire.

Le premier instantané de l'année était réelement énorme! Ainsi l'instantané 20190108 a mis à jour plus d'une centaine de paquets!
La suite **KDE Application 18.12.0** a été mise à jour et plus de 140 corrections de bogues ont été apportées à des applications telles que Kontact Suite, Cantor, Dolphin, Gwenview, KmPlot, Okular, Spectacle, Umbrello, etc.
La mise à jour de **curl 7.63.0** comportait un correctif pour l’analyseur d’adresses numériques IPv6 ainsi que plusieurs autres correctifs et une reprise de la session de support avec le protocole TLS 1.3 via OpenSSL.
**Apparmor 2.13.2** a corrigé une erreur de syntaxe dans *rc.apparmor.functions*, pouvant provoquer des échecs de chargement de la stratégie.
Le noyau **Linux 4.19.12** était dans le premier instantané de l'année et devrait se rapprocher de la dernière version stable dans les prochaines semaines.
Divers correctifs et ajustements de compatibilité ont été apportés avec la mise à jour de **libreoffice 6.1.4.2**, qui supprimait certains correctifs.
Le format de compression **brotli 1.0.7** offre maintenant un décodage plus rapide sur ARM.
La dernière version de **claws-mail 3.17.3**, grâce à la prise en charge de l'indication de nom de serveur TLS (SNI), permet l'envoi d'un nom d'hôte, s'il est disponible, au serveur afin qu'il puisse sélectionner le certificat approprié pour un domaine. Cela est utile pour les serveurs qui hébergent plusieurs domaines sur la même adresse IP.
**Python-setuptools 40.6.3, qemu 3.1.0** et **squid 4.5** ont également été mis à jour.

Selon l'analyseur d'instantanés Tumbleweed, tous les instantanés se sont avérés plutôt stables, avec une note d'au moins 83, Il y a plus de 300 packages en attente, ils seront probablement publiés en plusieurs instantanés au cours des prochaines semaines.
