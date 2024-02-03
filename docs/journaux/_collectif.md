# Journal de création

## Semaine 9

## Semaine 8

## Semaine 7

## Semaine 6

## Semaine 5

## Semaine 4

## Semaine 3

## Semaine 2
Cette semaine a commencé d'une manière très mouvementée, Guillaume nous a annoncé qu'on devrait changer de logiciel pour le tracking de nos fiducials alors que nous avions déjà commencé à faire communiquer nos logiciels ensemble. Après plusieurs essais, nous sommes arrivé sur touch designer, nous avons maintenant du tracking dans le logiciel, mais également un petit problème: personne dans l'équipe n'est familier avec le Python, donc il faudra apprendre.

### La table
Nous avons déterminé que la table utiliserai un projecteur ultra short-throw, **celui-ci devant être élevé de 14"**, ce qui fait en sorte qu'il dépasse la table, il faudra donc déterminer une façon d'éviter que le projecteur brise l'immersion. Pendant que le côté pratique et technique de la table prend son temps, le côté artistique du projet progresse très bien, nous avons maintenant un style visuel qui est consistant parmis nos plusieurs éléments visuels, le côté jeu vidéo de la table est également en train de très bien progresser.

![Prototype de la table 1](medias/tablePrototype3.jpg)

![Prototype de la table 2](medias/tablePrototype1.jpg)

<br>

### En résumé
Notre projet a grandement progressé cette semaine, nous avons fait un pas à reculons pour deux en avant, le script présent dans touchDesigner est maintenant plus ou moins complètement fonctionnel, il ne reste qu'à calibrer le code avec la table, en d'autre lieu, nous n'avons toujours pas de caméra infrarouge, ce qui serait quelque-chose qui serait grandement aprécié d'obtenir au plus tôt possible.

## Semaine 1
Cette semaine, nous avons fait une grosse réunion d'équipe pour clarifier quelques points de notre projet.

![réunion avec l'équipe](medias/reunion_semaine_1.png)


Nous avons également fait les tests qui manquaient à faire, c'est-à-dire le test de l'apparition de l'image sur papier calque si un projecteur est présent derrière elle, aisni que la caméra infra-roughe pour détecter les fiducials présents sur les statuettes au travers du papier calque, nous pouvons maintenant réelement commencer à travailler sur notre projet.

### Détails du projet
Au cours de la semaine, nous avons solidifié nos idées sur le projet, beaucoup de ces choses peuvent être vus dans la préproduction, ici nous allons aller plus en détail sur le ce qu'il se passe sur la table. Sur celle-ci, on peut observer un un système solaire entouré de plusieurs choses: d'autres planettes, des lunes et des astéroïdes. Cet arrangement est un bac à sable dans lequel l'intéracteur peut causer plusieurs effets en posant les statuettes sur la table. Il y a 5 statuettes: 
- Trou noir
- Trou blanc (un jour ce nom va changer)
- Éruption Solaire
- Champ Magnétique
- Second Soleil
<br>
Les effets des statues sont celles-ci:

#### Trou Noir
**Type**: Déplacement
<br>
**Description**: Le trou noir déplace les objets vers son centre, lorsqu'ils arrivent à cet endroit, ils sont détruits, par contre, si on retire le trou noir avant que les objets arrivent au centre, ils conservent leurs momentum, ce qui peut causer des scénarios intéressants, comme par exemple, envoyer un astéroïde quelque-part dans le système. Lorsqu'on tourne cette statuette, l'effet est soit augmenté où réduit.

#### Trou Blanc
**Type**: Déplacement
<br>
**Description**: Le trou blanc, comme son nom l'indique, est le contraire du trou noir, fidèle à cette idée, déposer cette statue va repousser les éléments près du point où la statue est posée. Cela peut créer énormément de conséquences qui n'avaient pas étée prévues si la taille de la zone repoussant les objets est sous-estimée. Faire tourner la statuette augmente la taille de la zone repoussant les éléments, avec une limite bien sûr.

#### Éruption Solaire
**Type**: Destruction
<br>
**Description**: L'éruption solaire est très simple, lorsqu'on pose la statue sur la table, un rayon va partir du soleil jusqu'à la statue, détruisant tout ce qui se trouve entre les deux points, cette statue ne permet pas beaucoup de surprises, sauf la première fois où quelqu'un l'essai, mais aucun bac-à-sable n'est complet sans un outil de destruction massive. Comme la statue ne sert que d'un point pour la fin d'un segment, nous n'avons pas encore eu d'idée pour l'effet arrivant lorsqu'on tourne la statuette.

#### Champ Magnétique
**Type**: Chaos
<br>
**Description**: Le champ magnétique crée une zone autours de l'endroit où la statue à été posée, dans cette zone, les objets en orbite vont commencer à avoir des réactions étranges, par exemple, elles pourraient commencer à changer la direction vers laquelle elles vont. Où bien commencer à secouer violement. Les effets sont aléatoires et peuvent avoir différents résultats, lorsque la statue est tournée, les effets sont intensifiées.

#### Second Soleil
**Type**: Déplacement Chaotique
<br>
**Description**: Le second soleil agis comme celui au centre de la table, les planettes font donc commencer à orbiter autours de celui-ci si elles s'approchent trop de son champ d'attraction, certaines intéractions sont également possible avec les autres statutes, par exemple, l'éruption solaire va également être lancée à partir du second soleil. Faire tourner la statue augmente ou réduit l'effet.

