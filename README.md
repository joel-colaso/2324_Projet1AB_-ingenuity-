# Mars 2020 est une mission spatiale qui consiste à déployer l'astromobile (rover) Perseverance sur le sol martien pour étudier sa surface et collecter des échnatillons du sol. Elle constitue la première d'une série de trois missions dont l'objectif final est de ramener ces échantillons sur Terre pour leur analyse. 

Ingenuity est un petit hélicoptère développé par l'agence spatiale Américaine, la NASA. Il est mis en oeuvre à titre expérimental sur le sol de la planète Mars au cours de la mission Mars 2020.
L'hélicoptère est embarqué à bord du rover Perseverance. 

Le 19 avril 2021, pour la première fois dans l'histoire de l'ère spatiale, un engin effectue un vol motorisé dans l'atmosphère ténue d'une autre planète. L'objectif d'Ingenuity est la reconnaissance optique du terrain, l'hélicoptère réalise de nombreuses photos aériennes utiliées par les pilotes de l'astromobile Perseverance pour identifier les obstacles et les sites prometteurs (prelèvement d'échantillons rocheux sur le sol martien). 

Ingenuity est un hélicoptère de 1,8 kg disposant de 2 rotors contrarotatifs coaxiaux. Il tire son énergie de 6 batteries lithium-ion rechargées par des cellules solaires. Son système de navigation lui permet de suivre sans intervention humaine un trajet pré-programmé. Sa seule charge utile est une caméra. 

La mission s'est récemment arrêtée (18 janvier 2024) en raison de la casse d'un pale lors du 72e vol. 

Ingenuity a ouvert de nouvelles perspectives pour l'exploration de Mars. La NASA et l'ESA, dans leur mission de retour d'échantillons martien, incluent maintenant 2 hélicopères similaires qui seront chargés de collecter les tubes contenant les échantillons martien déposés par l'astromobile Perseverance en cas de panne de celui-ci. 

Dans  ce projet, nous allons tâcher de reproduire le module Ingenuity. 

![Photo ingenuity](https://github.com/joel-colaso/2324_Projet1AB_-ingenuity-/assets/161329228/e31ebabd-f48c-485a-bf0c-799dc236c984)

# Notre Projet
Notre projet est donc d'essayer de réaliser cet hélicopètre en mode miniature. C'est à dire que l'on veut créer un véhicule pouvant se déplacer dans les airs et prendre une photo de ce qu'il se passe en dessous. Pour  ela, nous disposons d'un total de 10 séances où nous devrons mélanger PCB, codage, soudage, etc.

# Equipe
Pour ce projet notre équipe est composée de quatres élèves en première années d'écoles d'ingénieur : l'ENSEA. Il est important de souligner ici que certains membres de ce projet sont passionnés par l'aérospatial, ce qui donc motive d'avantage ce dernier. Étant tous différents, nous disposons donc de compétences variées. Entre autres quand certains codent, d'autres s'occupent de la soudure ou de la réalisation du PCB. 

# Journal de bord
C'est ici que nous résumerons, séance par séance les avancées du projet. 

## Séance 1
### Réflexion autour du projet : documentation
Alors que nous avions directement l'idée d'Ingenuity, il est important de savoir où nous nous aventurons. Nous nous sommes donc renseignés sur les hélicoptères de base, puis sur ceux mono-axe, pour enfin lire diverses documentations sur le véhicule de la NASA.
Ensuite, est venu le temps des questions plus détaillées : comment peut-on le refaire ? Quels moteurs ? Combien ? Doit-on utiliser un seul axe ou plusieurs ? Comment le faire avancer/reculer ? Etc.

## Séance 2
### Premiers détails : Schémas et Cahier Des Charges
Lors de cette deuxième séance, nous avons concrétisé nos découvertes. Nous nous sommes principalement basés sur des schémas, plus ou moins vulgarisés. C'est donc lors de celle-ci que notre schéma d'architecture a commencé à prendre forme.

De plus, nous avons réfléchi à comment faire avancer notre hélicoptère. La question se pose ici, car en réalité, les pâles s'inclinent vers la direction souhaitée, ce qui n'était pas réalisable pour nous car il nous aurait fallu imprimer des pièces de taille bien trop petites, ou bien trop compliquées à souder par la suite. Nous devions donc réfléchir à une alternative. C'est ainsi que nous avons eu l'idée d'un poids se baladant dans la coque de notre hélicoptère. Ce dernier incline en réalité tout l'hélicoptère et non seulement les hélices.
Enfin, afin de conclure cette séance productive, nous avons tout juste débuté le schéma d'architecture de notre système.
(Tous les documents cités sont également disponibles sur le git dans le dossier "Schematics").

## Séance 3
### Schéma d'Archi : un pas important
Lors de cette troisième séance, nous nous sommes principalement concentrés sur le schéma d'architecture et tout ce qui l'entoure. Nous avons donc recherché avec plus de détails quels composants nous allions utiliser (transistor, régulateur de tension, ...) et une fois trouvés, nous avons fouillé afin de trouver leur datasheet respective. C'est donc ici que notre liste des composants nécessaires a commencé à prendre forme. Entre les résistances, les capacités et les connecteurs, la liste peut sembler longue.

En somme, nous avons donc finalisé le schéma d'architecture puis rassemblé au sein d'un document tous les composants nécessaires à notre projet. À la fin de cette séance, nous avons d'ailleurs commandé ceux que nous n'avions pas à notre disposition.

## Séance 4
### PCB et codage 
Quatrième semaine de projet, début de la réalisation du PCB de notre hélicoptère. Notre schéma d'architecture étant fini et validé par notre encadrant, nous pouvons donc passer à la réalisation de notre PCB. Dans un premier temps, nous avons donc juste retranscrit notre schéma d'architecture sur un schéma PCB en liant nos différents composants électroniques avec leurs entrées et sorties respectives. 

![Schema PCB](https://github.com/joel-colaso/2324_Projet1AB_-ingenuity-/assets/161328781/7a225ad6-0fcb-4feb-8c49-53c13f148fa4)

Cepednant, pour faire cela, il y a certains éléments dont nous avons du faire l'empreinte nous même tel que LDO que nous utilisons car il étati indisponible sur KiCAD. 

Au niveau du codage, nous avons juste continué à prendre en main le servo moteur à base de vidéos youtube et différents tests comme simplement lui faire faire des aller-retours. 

## Séance 5
### Routage et toujours codage
Le schéma du PCB est terminé, il ne nous reste plus que la dernière étape, aussi fastidieuse soit elle : celle du routage. Notre objectif est le suivant : optimiser au mieux la place ainsi que la masse. En effet, il ne faut pas que notre hélicopètre ne pèse trop lourd, il ne décollerait donc pas du sol. 

![Routage PCB](https://github.com/joel-colaso/2324_Projet1AB_-ingenuity-/assets/161328781/8dc03480-77e4-458a-946a-4493e380b637)

Le PCB est donc prêt à être envoyé à l'usinage, c'est donc ce que nous faisons et il ne nous restera plus que la soudure à faire. Il ne reste plus qu'à attendre sa réception maintenant. 

Pour le codage, cette fois les servomoteurs tournent cette fois-ci bien. Désormais, nous nous attaquons à la commande de l'angle de ces derniers. Pour cela, nous créons des fonctions prenant comme paramètre l'angle.  

## Séance 6
### Soudure, Github et encore du codage...
La moitié des séances ont été faites, et nous voyons de plus en plus notre projet se concrétiser malgré une certaine crainte sur le temps nous restant. Maintenant, on a reçu notre PCB, nous allons donc souder tous nos composants dessus. Pour cela, deux des membres de notre projet s'en occupe, l'un soude pendant que l'autre lui indique les directives (quel élément placé et où). Pour cela, ces deux derniers s'appuient beaucoup sur le BOM proposé par KiCAD. 

[INSERER BOM]

Au niveau du codage, les deux autres membres s'entraident afin d'améliorer au mieux nos fonctions et donc d'optimiser le temps d'éxécution. Les fonctions sont donc créées permettant à un servomoteur de tourner jusqu'à un certain angle donné. 

De plus, le git a été mis à jour car jusque maintenant, on n'uploadait nos divres fichiers et non les pushait. Ainsi, nous avons donc appris à se servir de git dans l'objectif de ne plus jamais upload et juste push.

## Séance 7
### Fin de la soudure, Reflexion sur le montage, mise en page et puis ... du codage
Lors de la dernière séance, un nous avions soudé un élément qui n'était pas le bon. Ainsi, nous avons du le désouder pour resouder le bon cette fois-ci. 

Suite à ça, nous avons encore une fois divisé le travail en deux équipes différentes. Une s'occupaient de continuer le codage pendant que l'autre commençait la modélisation (puis l'impression) 3D de toute la structure de notre Ingenuity. Nous avons donc imprimé au total une base inférieure carrée, quatres pattes permettant de le voir se poser ainsi qu'une base supérieure. Nous nous sommes très fortement inspiré du vrai véhicule de base quant à sa structure. 

Ensuite est venu une reflexion importante, si ce n'est nécessaire pour faire se déplacer notre véhicule dans toutes les directions possibles et non juste diminuer et monter en altitude. Ainsi, nous avons eu ensemble l'idée d'un système de "balancier" s'appuyant beaucoup sur le centre de gravité de ce dernier. Nous plaçons une masse qui selon sa position par rapport à ce dernier le fera se déplacer. Entre autres, si le masse se situe au nord du centre de gravité, alors l'hélicoptère avancera. Alors que s'il se situe à sa droite, l'hélicoptère se déplacera vers .... la droite. 

[Insérer schéma masses déplacement]

Il faut donc désormais concrétiser cette reflexion et coder ce qui va avec. Nous avons donc coder six fonctions différentes : Nord-Ouest, Sud-Ouest, Sud, Sud-Est, Nord-Est et Nord. Selon la fonction, l'angle des servomoteurs est différents. Voici quelques exemples : 

[Inserer schéma Nord-Ouest, Sud]


## Séance 8

## Séance 9

## Séance 10

# Livrables
## PCB
> Présentation du schéma (grandes lignes) + PCB

## Code
> Architecture de votre code

## Rendu final
> Video ici de votre projet
