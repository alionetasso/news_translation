---
title: "openSUSE développement: Compte rendu du sommet des constructions reproductibles 2018"
date: 20-12-2018 22:39 
layout: post
---
17 December 2018 par bmwiedemann.

La semaine dernière, j'ai assisté au sommet mondial des constructions reproductibles à Paris.
C'était très bien organisé par Holger, Gunner et leurs aides cachés à l'arrière-plan. Très similaire aux 2 derniers sommets auxquels j'ai assisté à Berlin.

Comme nous étions environ 50 participants, les introductions et les annonces ont été les seules choses à faire dans le grand groupe. Tous les travaux réels se sont déroulés dans 5-10 cercles plus petits.

Nous avons eu des participants de grandes entreprises comme Google (avec bazel), MicroSoft et Huawei, mais également de nombreuses distributions et projets open source. Même MirageOS en tant que système d'exploitation non Linux.

Nous avons partagé les connaissances, affiné les définitions des termes, développé des concepts tels que les «reconstructeurs» pour la vérification des versions et permis aux utilisateurs de faire davantage confiance aux logiciels qu’ils installent, etc.

J'ai entendu parler du [dump de base de données non documenté](https://tests.reproducible-builds.org/reproducible.sql.xz) (153 Mo) et du [schéma de base de données](https://tests.reproducible-builds.org/reproducibledb.html)

Et nous avons eu un peu de temps de piratage, aussi, alors il y a maintenant
un [travail jenkins](https://jenkins.debian.net/job/reproducible_opensuse_import_json/) qui affiche la [liste des packages openSUSE Factory non reproductibles](https://tests.reproducible-builds.org/opensuse/factory/x86_64/index_FTBR.html).

De plus, [mon outil de maintenance](https://maintainer.zq1.de/?pkg=bash) dispose désormais d’un support supplémentaire pour la distribution Alpine Linux, grâce à l’aide de l’un de ses responsables: Natanael Copa.
Ceci est destiné à aider toute la collaboration entre distributions, pas seulement pour les builds reproductibles.

Il reste encore du travail à faire pour mieux utiliser Mitre CPE pour mapper les noms de paquetages d’une distribution à l’autre.

Je pense que l’un des grands avantages du sommet a été le réseautage et les discussions en cours, de sorte que nous avons plus de facilité à travailler les uns avec les autres sur Internet à l’avenir.

[Source](https://lizards.opensuse.org/2018/12/17/report-from-the-reproducible-builds-summit-2018/)
