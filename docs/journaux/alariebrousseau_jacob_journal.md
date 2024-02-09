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
## Semaine 5
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
## Semaine 6
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
