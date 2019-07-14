Au cours de la semaine 50/2018, Tumbleweed a reçu 4 instantanés: **1206, 1208, 1211** et **1212**.
Les principales modifications concernent les paquets suivants :

* Noyau Linux 4.19.7
* Ruby Rails 5.2.1.1 (modifications liées à CVE)
* Guile 2.2.4, mis à jour depuis la branche 2.0
* util-linux 2.33
* Mise à jour du thème XFCE4, comme annoncé dans la [liste de diffusion](https://lists.opensuse.org/opensuse-factory/2018-12/msg00078.html).

Il reste toutefois quelques *« gros morceaux »* en attente, même si certains font des progrès mineurs :

* glibc 2.28, Python 3.7, openssl 1.1.1 : le principal paquet bloquant, qui empêchait les paquets en attente de construire, a pû être identifié (perl5.28 provoquait une boucle sans fin dans *makeinfo* lors de l'exécution). La zone de *staging* est encore loin d’être prête, Python 3.7 étant notoirement incompatible avec Salt.
* Mesa 18.3
* LLVM7: échec de la construction de Rust avec LLVM7
* Nouvelle design de l'installateur : la barre latérale revient (indiquant où se trouve actuellement le flux de travail d'installation)
* PostgreSQL 11
* Noyau Linux 4.19.8
* Perl 5.28
* Qt 5.12.0
* Applications KDE 18.12.0

On dirait que la liste des changements en attente s'allonge de semaine en semaine, en partie du fait que de plus en plus de développeurs semblent occupés à préparer leurs vacances. Mais il y a en encore bien assez pour que Tumbleweed continue de rouler ! :)
