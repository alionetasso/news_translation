---
title: 'Mises à jour de GNOME, LLVM, Samba, Ruby dans Tumbleweed'
blog_url: /
show_sidebar: true
show_breadcrumbs: true
feed:
    limit: 10
content:
    items: '- ''@self.children'''
    limit: '15'
    order:
        by: date
        dir: desc
    pagination: '1'
    url_taxonomy_filters: '1'
---

![](https://news.opensuse.org/wp-content/uploads/2019/10/GNOME3.34-graphic-940x529.jpg)

Deux instantanés [openSUSE](https://www.opensuse.org/) [Tumbleweed](https://en.opensuse.org/Portal:Tumbleweed) ont été publiés cette semaine, mettant à jour plusieurs bibliothèques et une nouvelle version de [GNOME](https://www.gnome.org/), [Ruby](https://www.ruby-lang.org/en/), [Samba](https://www.samba.org/), [Mozilla](https://www.mozilla.org/en-US/) et le compilateur [LLVM](https://llvm.org/).

L'instantané [20191018](https://lists.opensuse.org/opensuse-factory/2019-10/msg00283.html) a fourni des mises à jour mineures pour [Mozilla Firefox](https://www.mozilla.org/en-US/firefox/new/) 69.0.3 et [Thunderbird](https://www.thunderbird.net/) 68.1.2. La mise à jour de [Firefox](https://www.mozilla.org/en-US/firefox/new/) a corrigé un bug qui invitait les utilisateurs de [Yahoo mail](https://mail.yahoo.com/) à télécharger des fichiers en cliquant sur les courriels et la mise à jour [Thunderbird](https://www.thunderbird.net/) a corrigé quelques problèmes ainsi que l'importation de contacts dans le carnet d'adresses à partir d'un fichier [CSV](https://en.wikipedia.org/wiki/Valeurs_séparées_par_des_virgules). La suite logicielle [GNOME](https://www.gnome.org/) a été mise à jour vers la version [3.34](https://www.gnome.org/news/2019/09/gnome-3-34-released/), qui pourrait être la version qui entrera dans [openSUSE Leap 15.2](https://en.opensuse.org/openSUSE:Roadmap). Cette version de GNOME, nommée [Thessaloniki](https://en.wikipedia.org/wiki/Thessaloniki), inclut des mises à jour visuelles pour un certain nombre d'applications et les paramètres de sélection d'arrière-plan ont également fait l'objet d'une refonte, ce qui facilite la sélection d'arrière-plans personnalisés. Les développeurs utilisant [GNOME 3.34](https://www.gnome.org/news/2019/09/gnome-3-34-released/) remarqueront davantage de sources de données dans [Sysprof](https://wiki.gnome.org/Apps/Sysprof) facilitant le profilage des performances des applications. Les améliorations apportées à [Builder](https://wiki.gnome.org/Apps/Builder) incluent un inspecteur intégré [D-Bus](https://en.wikipedia.org/wiki/D-Bus). Les liaisons Javascript pour GNOME ont également été mises à jour avec la version [gjs 1.58.1](https://launchpad.net/ubuntu/eoan/armhf/gjs/1.58.1-1) et la version [gtk3 3.24.12](http://www.linuxfromscratch.org/blfs/view/svn/x/gtk3.html) a corrigé un décalage de pointeur sous [X11](https://www.x.org/) et [Wayland](https://wayland.freedesktop.org/).
L'environnement d'exécution [Python2](https://www.python.org/downloads/) a été supprimé avec la mise à jour de [samba 4.11.0](https://www.samba.org/samba/history/samba-4.11.0.html); [python 3.4](https://www.python.org/downloads/release/python-340/) ou une version ultérieure est désormais requise.

L'instantané [20191018](https://lists.opensuse.org/opensuse-factory/2019-10/msg00283.html) apportait une mise à jour du nouveau langage de programmation [vala 0.46.3](http://www.linuxfromscratch.org/blfs/view/svn/general/vala.html) qui se concentre sur les développeurs GNOME. Le langage de programmation [ruby 2.6.5](https://www.ruby-lang.org/en/news/2019/10/01/ruby-2-6-5-released/) a corrigé une vulnérabilité d'injection de code avec trois autres [Vulnérabilités et expositions courantes](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures).
La paquet [Snapper d'OpenSUSE](https://en.opensuse.org/openSUSE:Snapper_Tutorial) 0.8.5 a été mis à jour pour permettre le suivi des commentaires dans les fichiers de configuration. Le noyau Linux a été mis à jour en 5.3.6. NetworkManager 1.18.4 a amélioré la gestion des règles de routage, des règles ajoutées en externe et des règles reprises après le redémarrage d'un service NetworkManager. Le package NetworkManager-applet 1.8.24 a ajouté la prise en charge de l'[authentification SAE](https://en.wikipedia.org/wiki/Authentication_Automatique_de_Equals) ([WPA3](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access#WPA3) Personnel).
Des correctifs de régression ont été apportés aux versions 2.62.1 de [glib2](https://developer.gnome.org/glib/) et de [glib-networking](http://www.linuxfromscratch.org/blfs/view/svn/basicnet/glib-networking.html); ce dernier a également inclus deux corrections de [fuite mémoire](https://en.wikipedia.org/wiki/Memory_leak).
Les autres paquets remarquables mis à jour dans l'instantané étaient [webkit2gtk3](https://webkitgtk.org/) 2.26.1, [libsoup](https://wiki.gnome.org/Projects/libsoup) 2.68.2, [grilo 0.3.10](http://www.linuxfromscratch.org/blfs/view/svn/gnome/grilo.html) et [dconf 0.34.0](http://www.linuxfromscratch.org/blfs/view/svn/gnome/dconf.html).

Selon le [commentateur de clichés Tumbleweed](http://review.tumbleweed.boombatower.com/), l’instantané a une cote stable de 92.

La plupart des mises à jour de l'instantané [20191016](https://lists.opensuse.org/opensuse-factory/2019-10/msg00176.html) concernaient des paquets [YaST2](https://yast.opensuse.org/). Un plantage causé par une méthode de *widget* a été corrigé dans yast2-network 4.2.23 et au moins 10 langues ont été mises à jour dans le package yast2-trans. Les personnes peuvent contribuer au projet en traduisant via l'instance [openSUSE's Weblate](https://l10n.opensuse.org/).
Il y avait une poignée d'autres paquets mis à jour dans l'instantané, mais le plus important à noter est une nouvelle version majeure de [llvm9](https://releases.llvm.org/9.0.0/docs/ReleaseNotes.html). La nouvelle version majeure du compilateur nécessite uniquement une base python3 au lieu des paquets python3 complets. L'optimiseur LLVM convertira désormais les appels à memcmp en appels à bcmp dans certaines circonstances. La version majeure ne considère plus non plus la cible [RISCV](https://en.wikipedia.org/wiki/RISC-V) comme "expérimentale". Il est maintenant construit par défaut, plutôt que d'avoir besoin d'être activé avec [LLVM\ EXPERIMENTAL\ TARGETS\_TO\_BUILD](https://stackoverflow.com/a/46908816/2487009).

Cet instantané a enregistré une note stable de 91, selon le [commentateur de clichés Tumbleweed](http://review.tumbleweed.boombatower.com/).