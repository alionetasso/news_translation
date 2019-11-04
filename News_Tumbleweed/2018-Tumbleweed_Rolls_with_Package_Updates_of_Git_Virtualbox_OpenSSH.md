Les cinq instantanés [Tumbleweed](https://en.opensuse.org/Portal:Tumbleweed) de cette semaine ont apporté le [noyau Linux](https://www.kernel.org/) 4.19.5, qui était le seul paquet mis à jour dans l'instantané [20181130](https://lists.opensuse.org/opensuse-factory/2018-12/msg00017.html). La version 4.19.5 du noyau a ajouté une option *force* pour les périphériques *pciserial* pour l’architecture [x86](https://en.wikipedia.org/wiki/X86) et a corrigé [HiperSockets](https://en.wikipedia.org/wiki/HiperSocket), un *sniffer* pour l'architecture [s390](https://en.wikipedia.org/wiki/IBM_System/390).

Le dernier instantané publié, [20181204](https://lists.opensuse.org/opensuse-factory/2018-12/msg00043.html), a mis à jour plus d'une douzaine de *packages*. L'application [GNOME](https://www.gnome.org/) pour gérer son compte d'hébergement d'images sur [Flickr](https://www.flickr.com/), [frogr](https: // wiki. gnome.org/Apps/Frogr) 1.5, les problèmes de contenu et d'installation du fichier AppData ont été résolus et le menu de fonctionnalités a été déplacé. L'application [GNOME](https://www.gnome.org/) *goffice* a été mise à jour en 0.10.44. Divers paquets [rubygem](https://rubygems.org/) ont été mis à jour et la modification la plus importante apportée aux paquets est que *rubygem-pry 0.12.2* a [supprimé la prise en charge](https://github.com/pry/pry/pull/1785) de [Rubinius](https://rubinius.com/). Python-boto3 1.9.57 et python-botocore 1.12.57 ont subi plusieurs modifications de l’interface de programmation (API). Le paquet *obs-service-set_version 0.5.11* avait besoin de «[python](https://www.python.org/) suff» et permet maintenant l'exécution de tests avec [python3](https://www.python.org/download/releases/3.0/).

Le premier instantané à arriver en décembre était le [20181203](https://lists.opensuse.org/opensuse-factory/2018-12/msg00026.html). Parmi les modifications apportées aux paquets, citons une mise à jour de [checkmedia](https://github.com/openSUSE/checkmedia) 4.1, qui corrigeait un bug dans *tagmedia*, du *framework* [GNOME](https://www.gnome.org/) de découverte des médias [grilo](https://wiki.gnome.org/Projects/Grilo) 0.3.7, et du compilateur distribué [icecream] (https://github.com/icecc/icecream) 1.2, qui a permis de mieux gérer les charge de calculs. Une dépendance de construction python-docutils a été ajoutée avec [cifs-utils 6.8](http://www.linuxfromscratch.org/blfs/view/svn/basicnet/cifsutils.html) et [elfutils 0.175](http: // www. linuxfromscratch.org/lfs/view/systemd/chapter06/libelf.html) a corrigé trois [vulnérabilités et expositions courantes](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures). Le paquetage [man 2.8.4](http://man-db.nongnu.org/) a apporté d’importants changements. L'une des modifications repose sur la lecture par les décompresseurs de leur entrée standard plutôt que par la transmission redondante du fichier d'entrée sur leur ligne de commande; cela fonctionne mieux avec le confinement des décompresseurs par [AppArmor](https://en.wikipedia.org/wiki/AppArmor). [Virtualbox](https://www.virtualbox.org/) 5.2.22 a corrigé une régression dans le *back-end* Core Audio, provoquant un blocage lors du retour de veille de l'hôte lors du traitement des tampons d'entrée et de [webkit2gtk3](https://webkitgtk.org /) 2.22.4 a corrigé des plantages et problèmes de rendu lors de l’utilisation de la bibliothèque graphique [Cairo](https://www.cairographics.org/) entre les versions 1.15 et 1.16.0.

L'instantané [20181129](https://lists.opensuse.org/opensuse-factory/2018-11/msg00328.html) n'avait que deux [KDE](https://www.kde.org/) paquets à mettre à jour. Ces paquets étaient [plasma-browser-integration](https://github.com/KDE/plasma-browser-integration) 5.14.4 et [xdg-desktop-portal-kde](https://github.com/KDE/xdg-desktop-portal-kde) 5.14.4. D'autres packages [Plasma 5.14.4](https://www.kde.org/announcements/plasma-5.14.4.php) sont attendus dans un prochain instantané.

Une mise à jour de Mozilla [Firefox 63.0.3](https://www.mozilla.org/en-US/firefox/63.0.3/releasenotes/) figurait dans l'instantané du début de semaine. La nouvelle version de [20181128](https://lists.opensuse.org/opensuse-factory/2018-11/msg00317.html) permet désormais à WebExtensions de s'exécuter dans son propre processus sous [Linux](https://www.linux.org/). L'outil de génération automatique de textes et de programmes [autogen 5.18.16](https://www.gnu.org/software/autogen/) prend en charge la compilation avec [Guile 2.2](https://www.gnu.org/s/guile) . Divers correctifs de bogues pour plusieurs sous-commandes et opérations ont été apportés avec la mise à jour dans [git 2.19.2](https://blog.github.com/2018-09-10-highlights-from-git-2-19/). [Mariadb 10.2.19](https://downloads.mariadb.org/mariadb/10.2.19/) avait une douzaine de correctifs CVE et recommande de désactiver la valeur par défaut pour ceux qui utilisent [XtraBackup](https://www.percona.com/software/mysql-database/percona-xtrabackup) au lieu de [Mariabackup](https://mariadb.com/kb/en/library/mariabackup-options/). Le paquet [openssh](https://en.wikipedia.org/wiki/OpenSSH) 7.9p1 interdit à présent l'utilisation de [clés DSA](https://en.wikipedia.org/wiki/Digital_Signature_Algorithm) pour une autorité de certification (nouvelle option CASignatureAlgorithms).

La mise à jour de [postfix 3.3.2](http://www.postfix.org/announcements/postfix-3.2.0.html) prend désormais en charge [openSSL 1.1.1](https://www.openssl.org/blog/blog/2018/09/11/release111) et [TLSv1.3](https://wiki.openssl.org/index.php/TLS1.3).

Tous les instantanés ont atteint un niveau de stabilité égal ou supérieur à 92, selon le [réviseur d’instantané Tumbleweed](http://review.tumbleweed.boombatower.com/).