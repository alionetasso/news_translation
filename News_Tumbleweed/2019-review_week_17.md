Quatre instantanés openSUSE Tumbleweed ont été publiés cette semaine. Ils fournissent un noyau Linux, des versions du framework KDE ainsi que python-setuptools pour offrir aux développeurs un grand nombre de nouveaux paquets upstream.

L'instantané Tumbleweed 20190423, le plus récent, fournissait un nouveau **cups-filters 1.22.5** qui modifiait un appel Ghostscript afin de corriger le nombre de pages pour qu'il fonctionne avec **Ghostscript 9.27** et les versions ultérieures.
Le package de décodeur AV1 **dav1d 0.2.2** apporte une augmentation de vitesse de 4 à 6% pour le décodage *MSAC (Multi Slot Amplitude Coding)* avec SSE. Le progiciel du noyau a été mis à jour en 20190409 et a mis à jour le fichier du micrologiciel pour les *firmwares* Intel Bluetooth et Marvell.
Des traductions indonésiennes ont été faites dans le paquet **libstorage-ng 4.1.112**.
**Ruby 2.6.3** a mis à jour la version Unicode vers la version 12.1 bêta pour ajouter la prise en charge de New Japanese Era “令 和” (Reiwa).
Les autres packages mis à jour dans l'instantané étaient **perl-DateTime 1.51, perl-DateTime-TimeZone 2.35, python-parso 0.4.0, python-qt5 5.12.1** et **rdma-core 23.0**.
Selon l'outil d'évaluation de Tumbleweed, cet instantané a actuellement une cote de 89.

**Mesa 19.0.2** présentait quelques correctifs pour radeon, radv et v3d dans l'instantané 20190420. Quelques autres paquets ont été mis à jour dans cet instantané, tels que **kipi-plugins 5.9.1**, qui était la première version autonome en dehors de **digikam**.
Selon l'évaluateur Tumbleweed, cet instantané affiche actuellement une côte de 97.

Les contributeurs de KDE ont proposé de nombreuses corrections et bibliothèques d'addons à Qt avec la mise à jour de **Frameworks 5.57.0** dans l'instantané 20190419. Le framework d'interface utilisateur légère de KDE pour les applications mobiles et convergentes, appelée **Kirigami**, comportait la plupart des mises à jour, ainsi que KIO et les fonctions de gestion de fichiers qu'elle fournit aux utilisateurs de Konqi.
**Python-setuptools 41.0.0** est un autre package destiné aux développeurs qui est arrivé dans l'instantané. Le package supprime la prise en charge de la spécification d’un codage à l’aide d’une directive *«coding:»* dans l’en-tête du fichier. Lors de l'analyse des fichiers *setup.cfg*, **setuptools** exige désormais que les fichiers soient encodés en UTF-8.
**Java-11-openjdk** mis à jour en 11.0.3.0 a ajouté des scénarios de test pour une analyse syntaxique japonaise et a implémenté plusieurs correctifs de sécurité.
Cet instantané affichait une note stable de 97.

L'instantané qui a commencé la semaine, 20190418, affichait une note stable de 94.
L'instantané a mis à jour **ImageMagick** vers la version 7.0.8.40 et résolvait plusieurs problèmes suivis sur github.
Le paquet **emacs 26.2** est maintenant compatible avec la dernière version 11.0 du standard Unicode et des modifications ont été apportées aux modes et paquets spécialisés dans **Emacs 26.2 Dired**: la commande ‘Z’ d’un nom de répertoire compresse désormais l’ensemble de ses fichiers.
Le noyau **Linux 5.0.8** comportait des correctifs pour les plate-formes *arm* et autres. Une des mises à jour du noyau a corrigé les régulateurs du codec audio du processeur *AM335x Evaluation Module*.
Les autres packages mis à jour dans l'instantané étaient **hwdata 0.322, sshfs 3.5.2** et **yast2 4.2.0**, nécessaires pour charger des frameworks de tests d'intégration.
