Mise à jour des packages Mesa, VirtualBox, Ceph et NetworkManager dans Tumbleweed
---------------------------------------------------------------------------------

Le 6 juin 2019 par [Douglas DeMaio](https://news.opensuse.org/author/ddemaio/ "Posts de Douglas DeMaio")

![](https://news.opensuse.org/wp-content/uploads/2017/06/geekoshirt-212x300.png)

Trois instantanés [openSUSE](https://www.opensuse.org/) [Tumbleweed](https://en.opensuse.org/Portal:Tumbleweed) ont été publiés au cours des quatre premiers jours de juin, ce qui entraîne plusieurs mises à jour des paquets dans cette *rolling-release*.

L'instantané [20190604](https://lists.opensuse.org/opensuse-factory/2019-06/msg00087.html) apportait le paquet **babl 0.1.64**, améliorant la cohérence du code, la prise en charge de l'[intégration continue](https://en.wikipedia.org/wiki/Continuous_integration) (CI) de [gitlab](https://gitlab. com), ainsi que des améliorations d’autotools et [meson build](https://mesonbuild.com/).
Un accident dans la dénomination a entraîné le passage de la version 0.3.2 de **bubblewrap** à la version 0.3.3. Cependant, **bubblewrap** 0.3.3. a corrigé une vulnérabilité (CVE), fourni quelques corrections plus petites et ajouté l’API (Application Programming Interface) JSON qui permet de lire le code de sortie du processus interne.
[GNU Compiler Collection](https://gcc.gnu.org/) 8 a eu quelques mises à jour qui comprenaient quelques correctifs dont un rendant les constructions sans profilage reproductibles.
La bibliothèque Generic Graphics Library [gegl](http://gegl.org/) 0.4.16 a également ajouté le support de gitlab CI et utilise un allocateur personnalisé pour les données de mosaïque, qui aligne les données et les allocations de groupes dans des blocs ; ceci a été réalisé sur [Linux](https://www.linux.org/) en utilisant l'extension GNU *malloc\_trim* pour permettre de forcer l'invocation de la fonction de récupération de place d'allocateurs, [malloc](https://en.cppreference.com/w/c/memory/malloc), présente au sein de la [glibc](https://www.gnu.org/s/libc/).
La version 6.0.8 d’Oracle [virtualbox](https://www.virtualbox.org/) corrigeait un crash lors de la mise hors tension d’une machine virtuelle sans contrôleur graphique et la version 1.20.5 de **xorg-x11-server** en corrigeait certains types d'entrées.
L’instantané a actuellement une cote de 96, selon l'[évaluateur d’instantané](http://review.tumbleweed.boombatower.com/).

L'instantané [20190603](https://lists.opensuse.org/opensuse-factory/2019-06/msg00078.html) a mis à jour [Mesa](https://www.mesa3d.org/) et [Mesa-drivers]( https://www.mesa3d.org/) en version 19.0.5 améliorant certaines parties du code et des pilotes.
[NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) 1.16.2 a corrigé certaines autorisations erronées du fichier `/var/lib/NetworkManager/secret_key`.
La mise à jour de la version mineure de [Ceph](https://ceph.com/) a désactivé l'[Optimisation du temps de liaison](https://stackoverflow.com/questions/23736507/is-there-a-rreason-why-not-to -use-link-time-optimization-lto) dans le fichier *spec* lors de son utilisation.
[GNOME 3.32.2](https://www.gnome.org/news/2019/03/gnome-3-32-released/) comportait plusieurs mises à jour et correctifs de packages, notamment le correctif d'une régression qui entraînait la disparition de la catégorie "Fonts" (Polices).
Tumbleweed a zappé la série 1.3.0 de [Flatpak](https://flatpak.org/) pour fournir directement à la version 1.4.0. Les principales modifications depuis la version 1.2.4 concernent l'utilisation améliorée des Entrées/Sorties pour les applications installées sur le système et le nouveau format des dépôts préconfigurées.
[Glib2](https://developer.gnome.org/glib/) 2.60.3 a mis à jour les traductions et fourni diverses corrections au support des petites clés/valeurs dans [GHashTable](https://developer.gnome.org/glib/stable /glib-Hash-Tables.html). Le langage de script [php7 7.3.6](https://www.php.net/ChangeLog-7.php#7.3.6) a ajouté une [curl_version](https://www.php.net/curl_version) manquante et corrigé plusieurs autres bugs.
L’instantané a actuellement une côte de 95, selon l'analyseur d’instantané (http://review.tumbleweed.boombatower.com/).

L'instantané qui a commencé le mois, [20190601](https://lists.opensuse.org/opensuse-factory/2019-06/msg00022.html), a mis à jour le [Noyau Linux](https: //www.kernel. org /) en version 5.1.5, ce qui corrigeait un [bogue de perte de données](https://www.phoronix.com/scan.php?page=news_item&px=Linux-5.1.5-Released).
[Flatpak-builder](https://github.com/flatpak/flatpak-builder) 1.0.7 a corrigé quelques détails sur la façon de créer des validations de plate-forme afin de résoudre les problèmes liés à la mise en cache de polices.
La visionneuse d'images de GNOME [gthumb](https://wiki.gnome.org/Apps/Gthumb) 3.8.0 faisait partie des autres mises à jour de paquet contenues dans l'instantané en compagnie de **ibus-libpinyin 1.11.1**, **libopenmpt 0.4.5**, [qalculate 3.2. 0](https://qalculate.github.io/manual/index.html), [rdesktop 1.8.6](https://www.rdesktop.org/), qui corrigeait le code du protocole gérant les nouvelles licences, et **yast2-support 4.1.1**.
L’instantané a actuellement une cote de 90, selon l'analyseur d’instantané (http://review.tumbleweed.boombatower.com/).
