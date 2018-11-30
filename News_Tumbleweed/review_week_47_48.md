Chers utilisateurs et *hackers* de Tumbleweed,

Les deux dernières semaines ont été plutôt chargées en *snapshots* : si vous suivez à plein régime les mises à jour, vous avez reçu 7 nouveaux instantanés: 1116, 1118, 1120, 1122, 1126, 1128 et 1129.
Ces instantanés ont apporté principalement les mises à jour suivantes (et beaucoup d'autres, comme d'habitude):

* KDE Frameworks 5.52.0
* FFmpeg 4.1
* système 239
* Noyaux Linux 4.19.2 et 4.19.4
* Mozilla Firefox 63.0
* openSSH 7.9p1: la configuration par défaut n'autorise plus l'accès root à l'aide de password auth

Changements en cours de réalisation et de test:

* glibc 2.28, Python 3.7, openssl 1.1.1: les trois sont interdépendants et provoquent de nombreux échecs - Voir Staging: C
* LLVM7 / Mesa 18.2.x (Rust ne parvient pas à construire avec LLVM7)
* Nouveau *design* de l'installateur: la barre latérale revient (indiquant l'étape d'installation actuelle)
* PostgreSQL 11
* KDE Plasma 5.14.4
