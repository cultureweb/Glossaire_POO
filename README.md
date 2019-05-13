# Glossaire POO Programmation orientée objet

La programmation oriénté objet permet de structurer son code en pensant justement en **objet**. Par exemple, pour construire une voiture, il nous faut d’abord créer un moteur, des siéges, un volant… Mais faire une voiture en partant de rien c’est pas simple surtout si on est tout seul !

Une solution pour fabriquer cette voiture consiste à diviser le travail en équipe. Chaque équipe devra s’occuper d’une partie des composants de la voiture ( siége ou moteur…). La roue existe déja ! pourquoi la ré-inventé. On récupére ce qui existe déja ! Ensuite quand tout les composants sont terminés, on assemble le tout et on obtient notre voiture !

Cela semble évident! et bien la programmation orienté permet en autre de travailler de cette façons !
article inspiré de mon site web : [e-real.fr](https://www.e-real.fr)

##### 1_Le vocabulaire de la POO

##### 2_Le concept de la POO

##### 3_L'Oblet Vs Le Procédural

### 1\_ Le vocabulaire de la POO

Le terme le plus important est la **class**. Une class est le modèle ou le patron à partir duquel l'objet est fabriqué.
Lorsque vous créez un objet à partir d'une classe, on dit qu'on crée une instance de la classe.

`Car mercedesClassA = new Car() ;`

On crée une nouvelle instance de la class Car.
Objet : mercedesClassA
Class : Car

**Héritage**
Une caractéristique importante des langages orientés objet est l'héritage. Héritage fait référence à la possibilité de définir une nouvelle classe d'objets qui hérite d'une classe parente. Une classe fille hérite de toutes les méthodes et attributs de la classe mère. Cependant elle ne peut pas utiliser les attributs et méthodes en private. Elle devra donc utiliser les setters et getters correspondants.

**abstrait**
Un mot clé du langage de programmation Java (TM) utilisé dans une définition de classe pour spécifier qu'une classe ne doit pas être instanciée, mais plutôt héritée par d'autres classes. Une classe abstraite peut avoir des méthodes abstraites qui ne sont pas implémentées dans la classe abstraite, mais dans des sous-classes.

**classe abstraite**
On peut créer des classes abstraites pour empêcher de les instancier. Ces classes ne devront servir que dans le cadre d’un héritage.

**méthode abstraite**
On peut aussi déclarer une méthode comme étant abstraite, dans ce cas, toutes les classes filles devront la réécrire. Ceci vise à forcer les classes filles à écrire une méthode donnée. Cependant, on n’inscrira aucune instruction dans la méthode de la classe mère.

**Interfaces**
Une interface est une classe complètement abstraite. Elles sont différentes de l’héritage car elles ne représentent pas un sous-ensemble, elles décrivent un comportement à un objet. Ainsi, il est logique que des classes voiture et moto héritent d’une classe véhicule, mais pas la classe son. En revanche toutes ces classes peuvent implémenter l’interface vitesse, car voiture comme moto ou son, ont une vitesse de déplacement.
