Tumbleweed obtient un nouveau grep, noyau Linux 4.20
-------------------------------------------

25 janvier 2019 par [Douglas DeMaio](https://news.opensuse.org/author/ddemaio/)

![](https://news.opensuse.org/wp-content/uploads/2016/05/Tumbleweed-black-green-300x127.png)

Un total de deux instantanés est arrivé dans [openSUSE](https://www.opensuse.org/) [Tumbleweed](https://en.opensuse.org/Portal:Tumbleweed) depuis l'article de la semaine dernière.

Les deux instantanés ont fourni les nouvelles versions de [grep](https://www.gnu.org/savannah-checkouts/gnu/grep/manual/grep.html), [VLC](https://www.videolan.org/ index.html), [Applications KDE](https://www.kde.org/announcements/announce-applications-18.12.1.php) et [Frameworks](https://www.kde.org/announcements/kde-frameworks-5.54.0.php), [Thunderbird](https://www.thunderbird.net/en-US/thunderbird/60.4.0/releasenotes/), [wirehark](https://www.wireshark.org/download.html) et plus.

Le dernier instantané, [20190121](https://lists.opensuse.org/opensuse-factory/2019-01/msg00370.html), a fourni des mises à jour de [KDE Applications 18.12.1](https://www.kde.org/announcements/advert-applications-18.12.1.php) et [Frameworks 5.54.0](https://www.kde.org/announcements/kde-frameworks-5.54.0.php).
[Applications 18.12.1](https://www.kde.org/announcements/announce-applications-18.12.1.php) propose environ 20 corrections de bugs.
Le tri des colonnes dans le lecteur [JuK music](https://www.kde.org/applications/multimedia/juk/) a été corrigé et [Akregator](https://userbase.kde.org/Akregator) fonctionne désormais avec [WebEngine](http://doc.qt.io/qt-5/qtwebengine-index.html) à partir de [Qt 5.11](https://wiki.qt.io/New_Features_in_Qt_5.11) ou plus récent.
[Konsole](https://konsole.kde.org/) rend à nouveau correctement les caractères de type *bos-drawing*.
La suite d'[icônes Breeze](https://github.com/KDE/breeze-icons) a ajouté l'icône [YaST](https://en.wikipedia.org/wiki/YaST) ainsi que de nouvelles icônes de préférences avec la mise à jour de [Frameworks 5.54. 0](https://www.kde.org/announcements/kde-frameworks-5.54.0.php). Celle-ci a également corrigé un bogue dans [KIO](https://api.kde.org/frameworks/kio/ html/index.html).
[Kwayland](https://github.com/KDE/kwayland) a corrigé l'en-tête de client [XDGForeign](https://github.com/wayland-project/wayland-protocols/tree/master/unstable/xdg-foreign).

La prise en charge du décodage 12 bits de [AV1](https://en.wikipedia.org/wiki/AV1) a été ajoutée à [vlc 3.0.6](https://www.videolan.org).
Une mise à jour mineure de [Collection du compilateur GNU](https://gcc.gnu.org/) 8 inclut un backport de [asm inline](https://gcc.gnu.org/onlinedocs/gcc/Extended-Asm.html ).
L'environnement de développement intégré léger [geany 1.34.1](https://www.geany.org/download/releases) détecte désormais automatiquement la version [GTK](https://www.gtk.org/) à utiliser.

Un correctif a été apporté à la mise à jour de [java-12-openjdk](https://openjdk.java.net/projects/jdk/12/) 12.0.0.0~26, introduisant un indicateur de diagnostic pour abandonner les machines virtuelles fonctionnant trop longtemps.
Un correctif pour [Mariabackup](https://mariadb.com/kb/en/mariabackup/) qui [échouait à faire des copies](https://jira.mariadb.org/browse/MDEV-18105) des tables système [InnoDB](https://en.wikipedia.org/wiki/InnoDB) des numéros de séquence de journaux (LSN) chiffrées a été créé avec [mariadb 10.2.21](https://mariadb.org/mariadb-10-2-21-maintenant disponible/).

L'outil de fusion et de comparaison visuelle [fusion 3.20.0](http://meldmerge.org/) a ajouté un raccourci « Entrer en tant que comparaison » dans les comparaisons de dossiers.
La mise à jour de [mutt 1.11.2](http://www.mutt.org/) a corrigé une erreur de compilation avec la dernière version de [OpenSSL](https://www.openssl.org/) ainsi que divers autres correctifs.
Plusieurs paquets [rubygem](https://rubygems.org/) ont également été mis à jour dans l'instantané. Deux problèmes récents ont été corrigés dans le package [purple-facebook 0.9.6](https://github.com/dequis/purple-facebook); l'un a traité d'un échec d'obtention de [sync\_sequence\_id](https://github.com/dequis/purple-facebook/issues/349) et l'autre d'un échec de lecture d'en-tête fixe.
[Samba 4.9.4](https://www.samba.org/samba/history/samba-4.9.4.html) traitait deux CVE, dont la correction d'une [boucle CNAME](https://en.wikipedia.org/wiki/CNAME_record).

L’instantané qui a débuté la semaine était [20190115](https://lists.opensuse.org/opensuse-factory/2019-01/msg00193.html) et incluait la version 4.20.0 du [Kernel Linux](https:// www .kernel.org /) et Mozilla [Thunderbird 60.4.0](https://www.thunderbird.net/en-US/thunderbird/60.4.0/releasenotes/), qui a ajouté l’API WebExtensions FileLink.
Plus de 30 améliorations de performances ont été apportées avec la mise à jour de [grep 3.3](https://www.gnu.org/s/grep/manual/grep.html).
Le package [Architecture sonore avancée de Linux](https://www.alsa-project.org/) [alsa 1.1.8](https://wiki.archlinux.org/index.php/Advanced_Linux_Sound_Architecture) a supprimé des correctifs obsolètes et ajout d'un paramètre de gestion unifiée des modifications (UCM) pour les plateformes [Dell Edge IoT](https://www.dell.com/en-us/work/shop/gateways-embedded-computing/sf/edge-gateway).
[Bison, un générateur d’analyseur](https://www.gnu.org/software/bison/) a été mis à jour vers la version 3.2.4.
Une mise à jour de l'application de gestion des informations personnelles de [GNOME](https://www.gnome.org/), [evolution](https://wiki.gnome.org/Apps/Evolution) 3.30.4, verrouille les valeurs de GSettings avant de restaurer la taille de la fenêtre.
Un saut a été effectué entre libvirt-glib 1.0.0 et 2.0.0 et il a permis de moderniser l’utilisation de la macro [gobject](https://developer.gnome.org/gobject/stable/).
Parmi les autres paquets remarquables mis à jour dans l'instantané, citons [gucharmap 11.0.3](https://wiki.gnome.org/action/show/Apps/Gucharmap?action=show&redirect=Gucharmap), [mercurial 4.8.2](https:/ /www.mercurial-scm.org/downloads), [python-pyOpenSSL 18.0.0](https://pyopenssl.org/), [sqlite3 3.26.0](https://www.sqlite.org) et [ Wirehark 2.6.6](https://www.wireshark.org/download.html).

Le snapshot [20190115](https://lists.opensuse.org/opensuse-factory/2019-01/msg00193.html) était plutôt instable avec une note de 61, selon [le réviseur d'instantanés Tumbleweed](http://review.tumbleweed.boombatower.com/). Le snapshot [20190121](https://lists.opensuse.org/opensuse-factory/2019-01/msg00370.html) quant à lui, est plus stable, avec une note de 78.
