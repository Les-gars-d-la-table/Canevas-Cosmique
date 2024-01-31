# Préproduction

# Table des matières
1. [Intention ou concept](#Intention-ou-concept)
    - [Cartographie](#Cartographie)
    - [Intention de départ](#Intention-de-départ)
    - [Synopsis](#Synopsis)
    - [Tableau d'ambiance (*moodboard*)](#Tableau-d'ambiance-(*moodboard*))
    - [Scénario, scénarimage ou document audio/visuel](#Scénario,-scénarimage-ou-document-audio/visuel)
2. [Contenu multimédia à intégrer](#Contenu-multimédia-à-intégrer)
    - [Inventaire du contenu multimédia](#Inventaire-du-contenu-multimédia)
    - [Univers artistique des éléments](#Univers-artistique-des-éléments-centraux)
3. [Planification technique d'un prototype (devis technique)](#Planification-technique-(devis-technique))
    - [Schémas ou plans techniques](#Schémas-ou-plans-techniques)
    - [Matériaux requis](#Matériaux-de-scénographie-requis)
    - [Équipements requis](#Équipements-requis)
    - [Logiciels requis](#Logiciels-requis)
    - [Ressources humaines requises](#Ressources-humaines-requises)
    - [Ressources spatiales requises (rangement et locaux)](#Ressources-spatiales-requises-(rangement-et-locaux))
    - [Contraintes techniques et potentiels problèmes de production](#Contraintes-techniques-et-potentiels-problèmes-de-production)
4. [Planification de la production d'un prototype (budget et étapes de réalisation)](#Planification-de-la-production-(budget-et-étapes-de-réalisation))
    - [Budget prévisionnel](#Budget-prévisionnel)
    - [Échéancier global](#Échéancier-global)
    - [Liste des tâches à réaliser](#Liste-des-tâches-à-réaliser)
    - [Rôles et responsabilités des membres de l'équipe](#Rôles-et-responsabilités-des-membres-de-l'équipe))
    - [Moments des rencontres d'équipe](#Moments-des-rencontres-d'équipe)

# Intention ou concept
## Cartographie

![cartographie](medias/brainstormVer2.png)

## Intention de départ
Donner le pouvoir à l'intéracteur de jouer avec un système solaire qui agit comme un bac à sable en utilisant divers outils.

## Synopsis
L'utilisateur interagit en déplaçant une statuette avec un fiducial, ceux-ci représentant les divers outils de manipulations disponible. Par exemple, on peux utiliser un trou noir pour bouger des planètes et/ou d'autres objets astronomiques et causer d'autres phénomènes astronomiques comme des éruptions solaires. Essentiellement, le système solaire est un bac à sable où on peux créer et démolir les planètes!

## Tableau d'ambiance (*moodboard*)
![Unity Moodboard](medias/moodboardUnity.png)


## Scénario, scénarimage ou document audio/visuel

<p align="center">
<img align="center" src='medias/scenarimage_1.png' width='500'>

<img align="center" src='medias/scenarimage_2.png' width='500'>

<img align="center" src='medias/scenarimage_3.png' width='500'>

<img align="center" src='medias/scenarimage_4.png' width='500'>

<img align="center" src='medias/scenarimage_5.png' width='500'>

<img align="center" src='medias/scenarimage_6.png' width='500'>

<img align="center" src='medias/scenarimage_7.png' width='500'>
</p>





# Contenu multimédia à intégrer
## Inventaire du contenu multimédia

-  statuettes (pour les utilisateurs-trices)
-  sons
-  paysages sonores
-  vfx d'animation 3D
-  source lumineuse



## Univers artistique des éléments

Univers contemplatif d'éléments reliés à l'espace avec plusieurs formes et couleurs qui pourront se mélanger entre eux.

# Planification technique d'un prototype (devis technique)
## Schémas ou plans techniques

![Sketch Table](medias/table_sketch.jpg)
> Schéma de la table déssiné par notre soudeur

### Plantation 

![cartographie](medias/plantation_studio.png)
![cartographie](medias/plantation_1.png)

### Schéma de branchement 

![schema_branchement](medias/schema_branchement_ver4.png)

## Matériel de scénographie requis

* Table
    * Matériaux: Bois, Aluminium, Acrylique, Spandex
    * 48" x 36", 30" de hauteur
* grand studio avec les murs amovibles

## Équipements requis

* Audio
    * 2 haut-parleurs
    * 4 fils XLR 3 conducteurs de 15' (M->F)
    * 1 carte de son

* Vidéo
    * 2 projecteurs vidéo shortrow
    * 3 système d'acrochage
    * 1 caméra infrarouge

* Électricité
    * 2 cordon IEC (pour l'alimentation des haut-parleurs)
    * 2 multiprise

* Réseau
    * Switch poe 2 ports
    * 5 Cables Ethernet
    * 2 Cables HDMI
    * 2 Receivers HDMI
    * 2 Sender HDMI
    * 1 Capture card

* Ordinateur
    * 1 ordinateur

* micro ordinateur
    * 1 raspberry pi    
    

## Logiciels requis

* [Touch Designer](https://derivative.ca/)
* [Unity 2019 lts](https://unity.com/)
* [Open stage control](https://openstagecontrol.ammd.net/)
* [Autodesk Maya](https://www.autodesk.com/ca-fr)
* [VCV Rack](https://vcvrack.com/)
* [OBS](https://obsproject.com)

## Ressources humaines requises

* Guillaume Arseneault.
* Thomas Ouellet Fredericks
* TTP
* Un soudeur

## Ressources spatiales requises

* Grand studio
  * Espace avec faux murs pour projection autours de la table.
* Salle des matrices
  * Accès à plusieurs ports ethernet, possibilité de pouvoir avoir notre ordinateur dans cette salle. Possiblement également l'espace de rangement pour les statues de remplacement.

## Contraintes techniques et potentiels problèmes de production

| Contrainte ou problème potentiel                     | Solution envisagée                                    | Commentaires                                                                                 |
|------------------------------------------------------|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Nous n'avons pas testé la caméra avec ReacTIVision   | Tester différentes caméras. | ReactIVision ne fait maintenant plus parti de notre projet. Nous l'avons remplacé par Touch Designer, notre projet contient maintenant du Python|
| Notre ordinateur doit pouvoir communiquer avec trop de choses en HDMI ou DisplayPort | Expérimenter des façons d'éviter d'avoir trop de choses connectées à l'ordinateur à la fois.| Problème réglé, maintenant nous n'avons qu'une seule projection|
|Nous ne pouvons pas faire la table nous-même. | Nous connaissons des soudeurs qui pourraient faire les parties métaliques pour nous.| Notre soudeur a confirmé qu'il allait pouvoir travailler sur la table a commencé à créer les plans. |

# Planification de la production d'un prototype (budget et étapes de réalisation)
## Budget prévisionnel

Matériel Requis: 

- 2 Plaques d'acrylique clair de 24"x36" avec 1/4 de pouce d'épaisseur: [Lien Vers Produit](https://www.homedepot.com/p/Falken-Design-24-in-x-36-in-x-1-4-in-Thick-Acrylic-Clear-Sheet-Falken-Design-ACRYLIC-CL-1-4-2436/308669666)
<br>

Prix: 103.34$

<br>

- Papier calque: [Lien Vers Produit](https://hachem.com/fr/rouleau-de-papier-calque-bienfang-24-x-20-verges-079946037180.html)

Prix: 15.70$

<br>

- Environ 40 statuettes

prix: +/- 150$

<br>

- Spandex: [Lien Vers Produit](https://fabricville.com/products/ima-gine-cotton-spandex-solid-black?_pos=5&_sid=7e2a5d5e5&_ss=r)

Prix: 17.49$/m

<br>

Total: +/- 287$ (Sans Taxes)

## Échéancier global
Étapes importantes du projet visualisé dans GitHub (*milestones*):  

*Dates importantes :*
- Remise de la vidéo d'intention: Lundi 5 Février
- Maquette de la table terminée : Lundi 19 février
- Tout terminer les assets : Jeudi 29 Février
- Fonctionnement total de tous les logiciels entre eux : Vendredi 1 mars
- Table terminée : Vendredi 9 mars
- Projet final test : Lundi 11 mars
- Présentation des projets devant public : Lundi 18 mars

## Liste des tâches à réaliser
Visualisation des tâches à réaliser dans GitHub selon la méthode kanban:  
https://github.com/orgs/Les-gars-d-la-table/projects/1/views/2

Inventaire des tâches à réaliser dans GitHub selon le répertoire d'*issues*:  
https://github.com/Les-gars-d-la-table/preproduction/issues

## Rôles et responsabilités des membres de l'équipe 

**Mikaël Tourangeau**
- Modélisation et impression 3D des statuettes. 

**Étienne Charron**
- Comité Technique et coordination technique (suivi du devis technique);
- Programmation du module Max d'effet et de contrôle audio;
- Construction de la table

**Quoc Huy Do**
- S'assure du bon fonctionnement de Unity;
- Coordination artistique;
- Installation et mise en place de la capture audiovidéo du projet en temps réel;
- Programmation du module Unity d'effets visuels et intégration dans Max.

**Jérémy Cholette**
- Création des paysages sonores
- Installation de l'équipement dans l'espace physique.

**Jacob Alarie-Brousseau**
- Coordination générale du projet (coordination de l'échéancier, du budget, suivi de la liste des tâches à réaliser, s'assurer de la répartition des rôles et des responsabilités des membres de l'équipe);
- Programmation de la détection des marqueurs sur TouchDesigner.
- Communication entre les plusieurs logiciels utilisés par OCS et NDI
- Construction de la table

## Moments des rencontres d'équipe
Hebdomadaire
- **lundi "9:30"h (1h)** : Rencontre de suivi de projet.
- **Vendredi "17h" (1h)** : Rencontre du suivi de ce qu'on a réaliser pendant la semaine
