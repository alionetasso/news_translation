Revue Tumbleweed de la semaine 52

Le rythme  des snapshots a été un peu plus calme et c'est donc seulement 5 clichés qui ont été publiés fin 2018.
N'avaient pas encore été couverts dans des revues antérieures les instantanés **1213, 1214, 1218, 1219 et 1224.**
Après cela, un soucis dans OBS nous a forcé à faire une pause et à ne pas créer de nouveaux instantanés.

Quoi qu'il en soit, les quelques modificiations qui ont été publiées avec ces 5 instantanés sont:

* Mesa 18.3.1 (mise à jour 18.1.x)
* Qt 5.12.0
* Noyaux Linux 4.19.8 et 4.19.11
* Mozilla Firefox 64.0
* Applications KDE 18.12.0
* KDE Frameworks 5.53.0
* Passez à LLVM 7
* Perl 5.28.0

Vitesse lente donc mais impact important. C'est bien de voir qu'autant de piles majeures ont pu être mises à jour / soumises / testées / publiées avant la fin de l'année.

Mais, comme vous en avez certainement l'habitude, openSUSE Tumbleweed ne serait pas appelé « *rolling-release* stable » s'il n'y avait pas beaucoup d'autres choses en attente. Et stable signifie que nous ne publions pas d'instantanés tant que les tests openQA soient réussis.
Il y aura donc des mises à jour majeures à prévoir dans les prochains jours / semaines:

* Nouvelle design de l'installateur: la barre latérale revient, indiquant où on se trouve le processus d'installation. Ceci est déjà vérifié dans Factory et prendra un peu de temps pour tout bien régler dans openQA. C’est aussi la raison principale pour laquelle aucun nouvel instantané n’a lieu pour le moment.
* glibc 2.28, Python 3.7, openssl 1.1.1: toujours en attente pour l'instant dans la mesure où Python 3.7 est connu pour être incompatible avec Salt.
De plus, certains cycles de construction dans Factory rendent presque impossible sa mise à jour en 3.7.
* Noyau Linux 4.20.
* tcl 8.6.9, qui casse actuellement la suite de tests de sqlite3.
