Mise à jour des packages LibreOffice, php, GTK dans Tumbleweed
-------------------------------------------------- -

31 janvier 2019 par [Douglas DeMaio](https://news.opensuse.org/author/ddemaio)

![](https://news.opensuse.org/wp-content/uploads/2017/09/release-is-coming-black-260x300.png)

Trois instantanés [openSUSE](https://www.opensuse.org/) [Tumbleweed](https://en.opensuse.org/Portal:Tumbleweed) ont été publiés cette semaine.

Les trois instantanés ont fourni les nouvelles versions de [php7](http://php.net/manual/en/migration70.new-features.php), [poppler](https://poppler.freedesktop.org/), [gtk3](https://developer.gnome.org/gtk3/3.0/) et [LibreOffice](https://www.libreoffice.org/).

Le premier instantané de la semaine a complété l'ensemble des mises à niveau de la suite [KDE Applications](https://www.kde.org/announcements/announce-applications-18.12.1.php) qui a fait son apparition dans les instantanés de la semaine dernière.

L'instantané le plus récent, [20190126](https://lists.opensuse.org/opensuse-factory/2019-01/msg00547.html), a apporté [libreoffice 6.2.0.3](https://www.libreoffice.org/ download /), ajoutant ainsi un correctif de compilation avec [java-11.2](https://jdk.java.net/11/). La nouvelle version inclut également un correctif soumis la semaine dernière qui fournit le rendu de base des organigrammes avec les objets [LibreOffice’s SmartArt](https://extensions.libreoffice.org/templates/smartart-objects-workaround-template). De nombreux correctifs de sécurité ont été apportés avec [java-11-openjdk 11.0.2.0](https://openjdk.java.net/projects/jdk/11/) incluant un traitement JPEG amélioré et des connexions au serveur Web.
Le passage de [btrfsprogs](https://github.com/kdave/btrfs-progs) 4.19.1 à 4.20.1 a apporté un nouvel [identificateur universellement unique] (https://en.wikipedia.org/Universally_unique_identifier) (UUID). De fait, une modification légère de l'UUID sans réécrire toutes les métadonnées est désormais possible dans la version la plus récente.

Il y avait un correctif pour [GVariant](https://developer.gnome.org/glib/stable/glib-GVariant.html) sur les tests de la [P6 microarchitecture i686](https://en.wikipedia.org/P6_microarchitecture) avec la mise à jour de [glib2 2.58.3](http://www.linuxfromscratch.org/blfs/view/cvs/general/glib2.html). La dernière version de [gnome-builder] (https://wiki.gnome.org/Apps/Builder), 3.30.3, utilise désormais *–frame* et *–thread* avec le [débogueur de projet GNU](https: // www. gnu.org/s/gdb/). Le *toolkit* graphique [gtk3 3.24.4](https://gitlab.gnome.org/GNOME/gtk/tree/gtk-3-24) présentait quelques correctifs pour Wayland et des traductions mises à jour.

Le package [mobile-broadband-provider-info](https://github.com/GNOME/mobile-broadband-provider-info) de [GNOME](https://www.gnome.org/) a été mis à jour après presque deux ans à la version 20190116; il fournit des paramètres mobile large bande pour différents fournisseurs de services et une fonctionnalité prépayée pour [Iliad telecommunications](https://en.wikipedia.org/wiki/Iliad_Italia) en Italie.
Plusieurs corrections de bugs ont été apportées avec [php7 7.3.1](http://php.net/ChangeLog-7.php), qui incluait une modification de timevalue pour la fonction [curl\_getinfo](http://php.net/ manuel/fr/ function.curl-getinfo.php).
Poppler et poppler-qt5 0.72.0 ont subi des modifications importantes pour éviter respectivement les cycles d'analyse PDF et les fuites de mémoire. Il convient de noter que les autres packages mis à jour dans l'instantané sont [snapper 0.8.2](https://doc.opensuse.org/documentation/leap/reference/html/book.opensuse.reference/cha.snapper.html), [wicked](https://en.opensuse.org/Portal:Wicked) et [YaST](https://en.wikipedia.org/wiki/YaST).

L'instantané [20190125](https://lists.opensuse.org/opensuse-factory/2019-01/msg00477.html) n'a apporté qu'une poignée de packages mis à jour. Le serveur de messagerie, contacts et calendrier [cyrus-imapd 2.4.20](https://www.cyrusimap.org/stable/imap/download/release-notes/2.4/x/2.4.20.html) a fourni un correctif pour un crash et un autre résolvant un chemin de socket configuré trop long pour sa mémoire tampon.
Le paquet sans description, [python-xcffib 0.6.0](https://pypi.org/project/xcffib/), a été mis à jour. Les packages qpdf 8.3.0 et yast2-schema 4.1.1 ont été mis à jour dans l'instantané. Les attaquants peuvent être contrecarrés par la mise à niveau du package de messagerie distribuée [zeromq 4.3.1](https://github.com/zeromq).

L'instantané [20190124](https://lists.opensuse.org/opensuse-factory/2019-01/msg00462.html) a effectué toutes les mises à niveau de l'environnement [KDE](https://www.kde.org/) [Applications 18.12.1](https://www.kde.org/announcements/announce-applications-18.12.1.php), qui propose environ 20 corrections de bugs.
Tumbleweed a commencé la semaine avec une mise à niveau du [Noyau Linux](https://www.kernel.org/) vers la version 4.20.2. Les traductions en indonésien et en espagnol ont été mises à jour avec la mise à jour libstorage-ng 4.1.78.
Dans nagios_4.4.3, plus d'une douzaine de problèmes ont été corrigés, notament une erreur de construction sur l'architecture [aarch64](https://en.wikichip.org/wiki/arm/aarch64).
Le lecteur de musique léger [pragha](https://github.com/pragha-music-player) 1.3.99 a ajouté un nouveau plug-in de visualisation et le gestionnaire de bureau à distance [remmina](https://remmina.org/) 1.3.0 apporte la détection automatique de la langue et retire une barre d'outils flottante dépréciée.
Une longue liste de modifications a été apportée avec le package [python-kiwi 9.17.1](https://pypi.org/project/kiwi/) et la suite de packages **yast2** impliquaient plusieurs modifications pour les packages réseau, pare-feu et apparmor.

Le snapshot [20190124](https://lists.opensuse.org/opensuse-factory/2019-01/msg00462.html) a enregistré un score de stabilité de 70, selon [le réviseur d'instantanés Tumbleweed]
(http://review.tumbleweed.boombatower.com /). Le snapshot [20190125](https://lists.opensuse.org/opensuse-factory/2019-01/msg00477.html) quant à lui, tend à être plutôt stable avec une note de 77 et le dernier en date, [20190126](https://lists.opensuse.org/opensuse-factory/2019-01/msg00547.html) tend à être stable avec un score de 88.
