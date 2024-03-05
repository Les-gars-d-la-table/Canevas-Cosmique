# Journal de Jacob Alarie-Brousseau
![portrait du participant ](../web/medias/participants/A.png)

* [Semaine 1](#semaine-1)
* [Semaine 2](#semaine-2)
* [Semaine 3](#semaine-3)
* [Semaine 4](#semaine-4)
* [Semaine 5](#semaine-5)
* [Semaine de rattrapage](#semaine-de-rattrapage)
* [Semaine 6](#semaine-6)
* [Semaine 7](#semaine-7)
* [Semaine 8](#semaine-8)
* [Semaine 9](#semaine-9)

## Semaine 1

### Résumé des réalisations effectuées
- Schémas de ce qui apparaît sur la table et ce qui apparaît sur le projecteur.

###
![iSchéma table](medias/jacobMedia/ViewTable.png)

### Est-ce que j'ai accompli l'ensemble des tâches et objectifs que je m'étais fixés pour cette semaine?	
- [x] Complètement
- [ ] Assez
- [ ] Peu
- [ ] Pas du tout

#### Décrivez pourquoi.
Nous avons maintenant une idée solide de ce que le projet va être, le rôle de touts les éléments ainsi que le style visuel de celles-ci, mon objectif cette semaine était de mettre tout au clair

### Mon projet s'est-il réalisé selon l’échéancier prévu?

- [ ] Complètement
- [x] Assez
- [ ] Un peu
- [ ] Pas tout à fait

#### S'il y a des écarts, décrivez-les.
Nous n'avons pas encore reçu les plans complets de la table.

#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?
Communiquer avec notre soudeur pour finaliser les plans.

### Défis pour la prochaine semaine
S'assurer que tous nos logiciels reçoivent les informations dont ils ont besoin.

---
## Semaine 2
### Résumé des réalisations effectuées
Ma semaine a commencée d'une manière relativement inatendue, j'ai dû remplacer un des logiciels au coeur de notre projet (reactivision), cela m'a mené à devoir écrire mes premières lignes de Python dans Touch Designer afin de créer un détecteur de marqueur, il est maintenant plus ou moins fonctionnel, je dois faire plus de tests dessus. Je sais par contre que je peux recevoir les informations dans unity, c'est une début, il faut juste que j'arrive à les séparer de la même manière que je les séparais dans Max. J'ai suivi un tutoriel pour la détection des marqueurs.

### Image d'une réalisation dont tu es la ou le plus fier

![Détection Touch Designer](medias/jacobMedia/detectionTouch.png)

### Est-ce que j'ai accompli l'ensemble des tâches et objectifs que je m'étais fixés pour cette semaine?

- [x] Complètement
- [ ] Assez
- [ ] Peu
- [ ] Pas du tout

#### Décrivez pourquoi.
 J'ai dû m'habituer à la syntaxe assez unique du Python et comprendre à peu près comment touchDesigner fonctionne sur le coup, j'ai réussi à détecter les marqueurs dans TouchDesigner et de envoyer l'information liée à ceux-ci dans Unity par OSC, pour ensuite les traiter correctement du côté de Unity. Nous avons également déterminé que le projecteur de la table devra être élevé de 14", ce qui est un peu triste parce que cela signifie qu'on va pouvoir le voir à côté de celle-ci.

#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?
Plus d'heures de travail.

### Mon projet s'est-il réalisé selon l’échéancier prévu?

- [ ] Complètement
- [x] Assez
- [ ] Un peu
- [ ] Pas tout à fait

#### S'il y a des écarts, décrivez-les.
Comme mentionné plusieurs fois maintenant, j'ai dû remplacer quelques logiciels que j'utilisais, ce qui est un contre-temps plutôt majeur, mais je pense que le progrès accompli par mes collègues contre-balance correctement. Les plans de la table devraient bientôt être terminés et on devrai avoir quelque-chose pour tenir le projecteur en place d'ici la semaine prochaine.

#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?
Plus d'heures de travail, demander de l'assistance de mes collègues pour mes tâches.

### Défis pour la prochaine semaine
Trouver une façcon de recevoir l'angle du marqueur, apprendre à calibrer la table.

---
## Semaine 3 
### Résumé des réalisations effectuées
J'ai commencé la semaine en créant une démo totalement jouable du produit final en combinant le travail de tout le monde dans la même scène sur Unity, j'ai également réussi à obtenir l'angle des marqueurs présentement détectés. J'ai ensuite passé la majorité de mon temps à trouver une manière de faire fonctionner notre table, que ce soit la caméra, l'angle du projecteur et la coupure de la projection. Détails sur les tests de caméra plus bas.

#### Détection de l'angle
J'ai créé le code de détection de l'angle en python, en gros, il se base sur la position des quatres coins du marqueur ainsi que de son centre pour calculer l'angle, voici une capture d'écran du code:
![image](https://github.com/Les-gars-d-la-table/Canevas-Cosmique/assets/93773873/2249a36b-7b63-4843-9ae3-a92a70aff2dc)
<br>
#### Démo Jouable
J'ai combiné les scripts de physiques avec les effets visuels créés par l'équipe et ajouté l'audio par dessus cela, j'en ai fait des prefabs, et j'ai adapté le code communiquant avec touchDesigner pour qu'il puisse démarer l'audio, créer les effets, et détruire les effets.

#### Tests pour la table
Les tests effectués par moi-même ont été ceux sur la caméra, j'ai essayé la kinect V1 et V2. Bien sûr, les caméras utilisées pour ces tests étaient les caméras infrarouge.
##### Kinect V1
Cette kinect était branchée sur un PI 400, le plan était d'envoyer le flux de la caméra par NDI vers l'ordinateur où la détection de marqueur est effectuée, pour qu'on puisse utiliser la caméra infrarouge du la V1, il fallait utiliser un filtre pour rendre l'image plus claire, malheureusement, l'image étant plus claire n'a pas aidé à la détection des marqueurs, qui n'étaient pas reconnus par touchDesigner. La résolution de la caméra était également trop petite, ne permettant pas de capter la surface complète de la table.
##### Kinect V2
Vendredi le 9 Février, j'ai testé la kinect V2, pour le moment, elle était directement connectée à notre tour, mais si nous conservons cette caméra, elle sera plus tard connectée sur un NUC. Cette caméra a une plus haute résolution que la kinect V1, et n'a pas besoin de filtre infrarouge pour marcher. Après avoir monté le contraste dans touchDesigner, elle détecte les marqueurs peu importe où ils sont sur la table sans trop de problème, il devient de temps en temps instable, mais je pense que c'est plutôt parce que les papiers sur lesquels les marqueurs sont ne sont plus droits, ce qui l'empêche de voir les 4 coins des marqueurs.
![markersDetected](https://github.com/Les-gars-d-la-table/Canevas-Cosmique/assets/93773873/dff45dd5-d1c3-4c0e-a288-72d5e4927ca5)
<br>
Pour le moment, je pense que nous allons nous servir de cette caméra dans version finale.
##### Spot sur l'acrylique
Au centre de l'acrylique se trouvait un spot blanc (voir image)
![Spot Blanc](https://github.com/Les-gars-d-la-table/Canevas-Cosmique/assets/93773873/1f0deff4-a141-46c1-867f-20f1e76a00cc)
<br>
Mon hypothèse était que c'était causé par le papier calque, mais en fin de compte, c'était réelement l'acrylique, à la recommendation de Guillaume, j'ai mis la caméra en angle, ce qui a réglé le problème.
![kinectAngle](https://github.com/Les-gars-d-la-table/Canevas-Cosmique/assets/93773873/352a764c-08aa-4aba-8cab-a7f3d84a6c70)
<br>

### Image d'une réalisation dont tu es la ou le plus fier
![tableFontionne](https://github.com/Les-gars-d-la-table/Canevas-Cosmique/assets/93773873/653bf82b-15c7-4275-aabf-3093713c64cd)



### Est-ce que j'ai accompli l'ensemble des tâches et objectifs que je m'étais fixés pour cette semaine?

- [x] Complètement
- [ ] Assez
- [ ] Peu
- [ ] Pas du tout

#### Décrivez pourquoi.
J'ai perfectionné le script de détection des marqueurs et combiné tout notre travail en une scène unity, et j'ai terminé la semaine en faisant fonctionner plus ou moins cette version de l'expérience sur notre maquette.

#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?


### Mon projet s'est-il réalisé selon l’échéancier prévu?

- [ ] Complètement
- [x] Assez
- [ ] Un peu
- [ ] Pas tout à fait

#### S'il y a des écarts, décrivez-les.


#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?


### Défis pour la prochaine semaine
Améliorer la projection, perfectionner nos effets pour la démonstration de la maquette du 19.
---
## Semaine 4
### Résumé des réalisations effectuées
Cette semaine, j'ai pas mal travaillé sur unity, j'ai créé une très grande liste de features, la destruction du système, un état inactif, la création de nouvelles planettes, resize la scène pour que celle-ci utilise une échelle de 1, créer un outil pour calibrer la table pendant que le jeu roule. J'ai également travaillé sur avoir une calibration plus précise en retravaillant le patcher TouchDesigner.

#### Destruction du système solaire
Lorsque le trou noir est posé sur le soleil, une animation démmare, si elle se termine, le système solaire est détruit et il faut retirer toutes les statues de la table pour que le système puisse redémarrer.

#### état inactif

Si aucune statue n'est présente sur la table pendant 2 minutes, elle entre un état inactif dans lequel de la musique joue.

#### Nouvelles planettes
À tous les 10 secondes, si moins de 15 planètes sont présentes dans la scène, il y a une chance sur 5 qu'une planète apparaîsse à chacun des coins, si il y a moins de 5 planètes, les chances sont augmentées à 1/3.

#### Outils de calibration
Comme nous ne pourrons pas toujours travailler avec l'éditeur de unity, il nous faut un interface dans lequel on peut calibrer la table, c'est le point de cet outils.

### Image d'une réalisation dont tu es la ou le plus fier

![tableFontionnelle](https://github.com/Les-gars-d-la-table/Canevas-Cosmique/assets/93773873/82438f47-05f0-41f5-85d7-a956a40e2bd7)


### Est-ce que j'ai accompli l'ensemble des tâches et objectifs que je m'étais fixés pour cette semaine?

- [x] Complètement
- [ ] Assez
- [ ] Peu
- [ ] Pas du tout

#### Décrivez pourquoi.
 J'ai pas mal litérallement travaillé sans arrêt pendant toute la semaine pour avoir toutes les features qu'on voulait dans le jeu. J'ai réussi à rentrer la majorité, le reste à été abandonné.

#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?


### Mon projet s'est-il réalisé selon l’échéancier prévu?

- [x] Complètement
- [ ] Assez
- [ ] Un peu
- [ ] Pas tout à fait

#### S'il y a des écarts, décrivez-les.


#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?


### Défis pour la prochaine semaine
 La semaine prochaine risque d'être beaucoup plus calme, nous avons tout nos systèmes fonctionnels donc tout ce qu'il nous reste à faire, c'est rajouter par dessus, polir notre projet, et peut-être changer un peu de visuel. Je n'ai pas vraiment de défi en tête mais comme nous allons reçevoir la table au courant de la semaine, je pense que calibrer le projet avec la table final sera le défi.
---
## Semaine 5
### Résumé des réalisations effectuées
Cette semaine, j'ai majoritairement travaillé sur améliorer le jeu sur Unity, reglé quelques bugs, ajouté quelques fonctions de qualité de vie et amélioré l'outil de calibration. J'ai également créé un système de sauvegarde pour le jeu, afin que celui-ci puisse retenir des informations lorsqu'on le ferme.

#### Bugfix et changements
- Réparé un bug qui causait le panel de destruction du système solaire sur le UI si on retirait la statue du trou noir avant les autres statues.
- Retiré l'état inactif de la table car il ne fonctionne pas avec notre prémisse.
- Réparé +/- le second soleil, si il est présent suffisement longtemps dans la scène, les planètes commencent à orbiter autours de lui.
- Changé les conditions pour le déclenchement de la destrucion du système solaire, maintenant les 5 statues doivent être sur le soieil pour que la séquence débute.
- Changé l'effet du trou noir sur le soleil, maintenant celle-ci consiste à augmenter la masse du soleil afin que toutes les planètes présentement dans la scène soient attirées.
- Réparé un bug visuel avec l'éruption solaire
- Ajout d'un système de sauvegarde afin de pouvoir conserver des données de calibration ainsi que certaines statistiques lorsque le jeu est éteint.
- Optimisation de code pour la détection (environ 700 lignes)
- Ajout d'un menu où on peut voir les statistiques qui sont comptabilisées par le jeu
- Ajout de la position présente du trou noir à l'interface de calibration de l'output, comme cela on peut s'en servir comme référence lorsqu'on calibre avec le jeu built.
- Ajout d'un nouvel effet visuel sur la projection murale lors de la destruction du système solaire
- Modifications de la position des murs autours de la scène afin d'empêcher les planètes de passer au travers des caméras.
- Création d'un système donnant des matériels aléatoires aux planètes lors de leurs apparition afin de créer plus de variété.
- Ajout de bruits lors de la collision entre planètes
- Changements au spawn des planètes, les chances d'apparitions originales n'ont pas changées, mais maintenant si il y a moins de 30 planètes, il y a une chance sur 10 d'en créer une nouvelle.

### Image d'une réalisation dont tu es la ou le plus fier

![image](https://github.com/Les-gars-d-la-table/Canevas-Cosmique/assets/93773873/5ee54a43-cfac-4db5-8445-1e236baa6eae)
Système de sauvegarde

### Est-ce que j'ai accompli l'ensemble des tâches et objectifs que je m'étais fixés pour cette semaine?

- [ ] Complètement
- [x] Assez
- [ ] Peu
- [ ] Pas du tout

#### Décrivez pourquoi.
 Cette semaine, je prévoyais majoritairement réparer quelques bugs dans le jeu pour rendre l'expérience meilleure et construire autours de ce que nous avions déjà créé, je pense avoir accompli adéquatement cet objectif. Le seul problème que je pourrai noter serai le second soleil, celui-ci agis de manière très étrange.

#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?


### Mon projet s'est-il réalisé selon l’échéancier prévu?

- [ ] Complètement
- [x] Assez
- [ ] Un peu
- [ ] Pas tout à fait

#### S'il y a des écarts, décrivez-les.
Nous sommes mainenant bientôt dans sixième semaine et nous n'avons toujours pas de sons avec des bons loops ainsi que les statues.

#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?


### Défis pour la prochaine semaine
La semaine prochaine va majoritairement tourner autours de l'installation physique ainsi qu'encore plus de polish sur le jeu, nous prévoyons avoir des extensions pour la table au courant de la semaine, les vraies statuettes, appliquer le spandex autours de la table et ajouter plus d'éléments à notre décor. La plus grande partie de la job est déjà passée alors maintenant ils ne nous reste qu'à s'assurer que notre expérience sois la plus immersive possible.
---
## Semaine 6
### Résumé des réalisations effectuées
Cette semaine, je me suis majoritairement concentré à m'assurer que les statuettes soient détectées correctement sur la table, nous ne savons pas exactement pourquoi, mais si le marqueur est imprimé directement dans la statuette, il n'est pas détecté dans le fond de la table. Après quelques jours de tests, nous avons décidé de rechercher des solutions. J'ai commencé par prendre un des marqueurs papier qu'on utilisait pour faire des tests, je l'ai plié pour qu'il prène la forme du dessous de la statuette, il était quand même détecté. Nous avons donc essayé de coller des stickers avec les marqueurs en dessous des statues, ce qui fonctionne, nous allons utiliser cette méthode pour la détection à partir de maintenant. En espérant que ceux-ci soient suffisament résistants. J'ai passé le reste de mon temps à debug le projet sur Unity, j'ai réparé certaines situations dans lesquelles l'éruption solaire ne fonctionnait pas. Réparé des bug avec l'intéraction sur le panneau de configuration. J'ai également été acheté le tissu qui va couvrir la table, finalement, je n'ai pas pris de spandex, parce que la table n'aurait pas pu respirer, j'ai été avec un tissu normalement utilisé pour des microphones, l'air passe au travers, mais il est loin d'être opaque, je pense que ça devrait être correct parce que lorsque les étudiants de première année sont venu voir nos maquettes, ils n'avaient pas l'air de se soucier que la table soit litéralement grande ouverte. Même qu'ils ne remarquaient pas la kinect sous leurs pieds.

### Image d'une réalisation dont tu es la ou le plus fier



### Est-ce que j'ai accompli l'ensemble des tâches et objectifs que je m'étais fixés pour cette semaine?

- [ ] Complètement
- [ ] Assez
- [ ] Peu
- [ ] Pas du tout

#### Décrivez pourquoi.
 

#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?


### Mon projet s'est-il réalisé selon l’échéancier prévu?

- [ ] Complètement
- [ ] Assez
- [ ] Un peu
- [ ] Pas tout à fait

#### S'il y a des écarts, décrivez-les.


#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?


### Défis pour la prochaine semaine

---
## Semaine de rattrapage
### Résumé des réalisations effectuées


### Image d'une réalisation dont tu es la ou le plus fier



### Est-ce que j'ai accompli l'ensemble des tâches et objectifs que je m'étais fixés pour cette semaine?

- [ ] Complètement
- [ ] Assez
- [ ] Peu
- [ ] Pas du tout

#### Décrivez pourquoi.
 

#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?


### Mon projet s'est-il réalisé selon l’échéancier prévu?

- [ ] Complètement
- [ ] Assez
- [ ] Un peu
- [ ] Pas tout à fait

#### S'il y a des écarts, décrivez-les.


#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?


### Défis pour la prochaine semaine

---
## Semaine 7
### Résumé des réalisations effectuées


### Image d'une réalisation dont tu es la ou le plus fier



### Est-ce que j'ai accompli l'ensemble des tâches et objectifs que je m'étais fixés pour cette semaine?

- [ ] Complètement
- [ ] Assez
- [ ] Peu
- [ ] Pas du tout

#### Décrivez pourquoi.
 

#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?


### Mon projet s'est-il réalisé selon l’échéancier prévu?

- [ ] Complètement
- [ ] Assez
- [ ] Un peu
- [ ] Pas tout à fait

#### S'il y a des écarts, décrivez-les.


#### S'il y a lieu, qu'allez-vous faire pour remédier à la situation?


### Défis pour la prochaine semaine


## Semaine 8


## Semaine 9
