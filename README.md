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
Une caractéristique importante des langages orientés objet est l'héritage. Héritage fait référence à la possibilité de définir une nouvelle classe d'objets qui hérite d'une classe parente. De nouveaux éléments de données et méthodes peuvent être ajoutés à la nouvelle classe, mais les éléments de données et méthodes de la classe parente sont disponibles pour les objets de la nouvelle classe sans réécriture de leurs déclarations.

**abstrait**
Un mot clé du langage de programmation Java (TM) utilisé dans une définition de classe pour spécifier qu'une classe ne doit pas être instanciée, mais plutôt héritée par d'autres classes. Une classe abstraite peut avoir des méthodes abstraites qui ne sont pas implémentées dans la classe abstraite, mais dans des sous-classes.

**classe abstraite**
Une classe qui contient une ou plusieurs méthodes abstraites et ne peut donc jamais être instanciée. Les classes abstraites sont définies afin que d'autres classes puissent les étendre et les concrétiser en implémentant les méthodes abstraites.

**méthode abstraite**
Une méthode qui n'a aucune implémentation.