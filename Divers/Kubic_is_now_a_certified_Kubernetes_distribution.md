Kubic devient une distribution certifiée Kubernetes
===================================================

*par Richard Brown sur [news.opensuse.org](https://news.opensuse.org/2019/01/24/kubic-is-now-a-certified-kubernetes-distribution/)*

L’équipe openSUSE Kubic est fière d’annoncer que sa distribution Kubic est devenue hier une distribution certifiée Kubernetes! Il s'agit notamment de la première distribution open source Kubernetes à être certifiée à l'aide de l'environnement d'exécution du conteneur CRI-O!

**Qu'est-ce que la certification Kubernetes?**

Les technologies de conteneurs en général, et Kubernetes en particulier, sont de plus en plus courantes et largement adoptées par les passionnés, les développeurs et les entreprises du monde entier. Un vaste écosystème de logiciels et de solutions évolue autour de ces technologies. De plus en plus de développeurs pensent «Cloud Native» et produisent d'abord leurs logiciels dans des conteneurs, ciblant souvent Kubernetes en tant que plate-forme destinée à orchestrer ces conteneurs. Et pour parler franchement, ils veulent que leurs logiciels fonctionnent.

Mais Kubernetes ne ressemble pas à un autre logiciel avec ce type d’adoption généralisée. Même s'il est utilisé dans des scénarios de grande et petite envergure, allant de petits laboratoires de développement à de grands systèmes d'infrastructure de production, Kubernetes reste un projet en évolution rapide. De nouvelles versions apparaissent très souvent et la durée de vie du support est plus courte que celle de projets similaires. Cela représente de véritables défis pour les personnes qui souhaitent télécharger, déployer et exécuter des clusters Kubernetes et qui savent qu’elles peuvent exécuter les tâches qu’elles souhaitent.

Si vous considérez la base de code en évolution rapide et la vaste gamme de solutions fournissant ou intégrant Kubernetes, vous obtenez de nombreuses pièces fournies par de nombreuses personnes. Cela peut sembler risqué pour certaines personnes et faire douter que quelque chose de construit pour Kubernetes aujourd'hui ne fonctionne pas demain.

Heureusement, la CNCF (Cloud Native Computing Foundation) s’attaque à ce problème. Le CNCF aide à créer une communauté autour du logiciel conteneur open source et a établi la certification de conformité du logiciel Kubernetes pour atteindre cet objectif. Les solutions Kubernetes certifiées sont validées par le CNCF. Ils vérifient que les versions, les API, etc., sont toutes correctes, présentes et fonctionnent comme prévu afin que les utilisateurs et les développeurs puissent être assurés que leurs solutions basées sur Kubernetes fonctionneront facilement, maintenant et à l'avenir.

**Pourquoi certifier Kubic?**

Le projet openSUSE s'attaque depuis longtemps au problème de la distribution de logiciels à évolution rapide.

Tumbleweed et Kubic sont simultanément deux des distributions de versions les plus rapides et les plus stables disponibles.
Avec Open Build Service et openQA, nous disposons d'un pipeline établi qui garantit que nous ne publions un logiciel que s'il est conçu et testé de manière collective et reproductible.

Notre expérience avec *btrfs* et *snapper* signifie que même en cas de modification non désirée d'un système, les utilisateurs peuvent immédiatement revenir à un état du système qui fonctionne comme ils le souhaitent.
Avec les mises à jour transactionnelles, nous veillons à ce qu'aucun changement ne survienne sur un système en fonctionnement. Cela garantit en outre que toute annulation peut ramener un système à un état propre en une seule opération atomique.

Dans Kubic, nous exploitons tout cela pour créer un excellent système d'exploitation de conteneur, fournissant aux utilisateurs les dernières versions de nouveaux outils passionnants tels que Podman, CRI-O, Buildah et (bien sûr) Kubernetes.
Nous nous tenons au courant de tous ces projets en cours d’amélioration rapide, en publiant souvent nos packages quelques jours voire quelques heures après leur publication en amont.
Mais nous veillons à ne pas mettre les utilisateurs en danger, à publier Kubic en synchronisation avec la plus grande distribution openSUSE Tumbleweed, à partager le même pipeline de tests et de publications, de sorte que nous puissions être sûrs qu'aucune des distributions n'apportent de modifications qui cassent l'autre.

Nous avons donc résolu tous les problèmes liés aux logiciels à évolution rapide, alors pourquoi certifier? 😉
Bien que cela me fasse mal d’écrire cela, peu importe à quel point nous sommes formidables avec la révision de code, la construction, les tests et la publication, nous ne pourrons jamais tout comprendre. Même si nous le faisions, à la fin de la journée, tout ce que nous pouvons dire, c’est *« nous faisons des choses formidables, faites-nous confiance »*.
Et quand vous considérez comment nous travaillons dans openSUSE, les choses peuvent sembler encore plus compliquées aux nouveaux arrivants.
Nous ne sommes pas comme les autres projets open source avec un bailleur de fonds qui tient les rênes et contrôle étroitement ce que nous faisons.

openSUSE est un projet de communauté véritablement open source où tout le monde peut contribuer, en prenant ce que nous faisons à Kubic et en le modifiant directement pour s’adapter à ce qu’ils veulent.
Ces contributions sont sur un pied d'égalité, SUSE et les autres sponsors d'OpenSUSE devant contribuer de la même manière que tout autre membre de la communauté.
Et nous voulons plus de contributions. Nous garderons Kubic ouvert et accueillant à toutes les idées folles (ou intelligentes ou incroyables) que vous pourriez avoir pour notre distribution de conteneurs.
Mais nous voulons aussi que tout le monde sache que quoi que nous fassions, les gens peuvent compter sur Kubic pour faire avancer les choses.

En certifiant Kubic auprès de la CNCF, une tierce partie impartiale a examiné ce que nous faisons, vérifié ce que nous distribuons, vérifié notre documentation et nous a donné son sceau d’approbation.

Donc, à tous ceux qui ont contribué à Kubic jusqu'à présent et qui ont rendu cela possible, MERCI! À tous les projets en amont sans lesquels Kubic n’aurait rien à distribuer, ni à certifier  MERCI et à bientôt sur vos *bugtrackers* et vos listes de *pull request*.

Et merci à tous et à toutes, MERCI, et nous espérons que vous aurez beaucoup de plaisir à télécharger, utiliser et, espérons-le, contribuer en retour à notre pierre dans l'édifice des conteneurs.
