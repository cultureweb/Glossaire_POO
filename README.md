# Glossaire POO Programmation orientée objet

La programmation oriénté objet permet de structurer son code en pensant justement en **objet**. Par exemple, pour construire une voiture, il nous faut d’abord créer un moteur, des siéges, un volant… Mais faire une voiture en partant de rien c’est pas simple surtout si on est tout seul !

Une solution pour fabriquer cette voiture consiste à diviser le travail en équipe. Chaque équipe devra s’occuper d’une partie des composants de la voiture ( siége ou moteur…). La roue existe déja ! pourquoi la ré-inventé. On récupére ce qui existe déja ! Ensuite quand tout les composants sont terminés, on assemble le tout et on obtient notre voiture !

Cela semble évident! et bien la programmation orienté permet en autre de travailler de cette façons !
article inspiré de mon site web : [e-real.fr](https://www.e-real.fr)

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

**Méthode abstraite**
On peut aussi déclarer une méthode comme étant abstraite, dans ce cas, toutes les classes filles devront la réécrire. Ceci vise à forcer les classes filles à écrire une méthode donnée. Cependant, on n’inscrira aucune instruction dans la méthode de la classe mère.

**Méthode surchargée**
Lorsqu'on définit une classe, on peut y définir plusieurs méthodes qui portent le même nom. La seule contrainte est que la liste des types des paramètres formels doit être différente. Ce mécanisme est appelé surcharge de méthode.

**Interfaces**
Une interface est une classe complètement abstraite. Elles sont différentes de l’héritage car elles ne représentent pas un sous-ensemble, elles décrivent un comportement à un objet. Ainsi, il est logique que des classes voiture et moto héritent d’une classe véhicule, mais pas la classe son. En revanche toutes ces classes peuvent implémenter l’interface vitesse, car voiture comme moto ou son, ont une vitesse de déplacement.

**Les getters et les Setters**
Les getters et les Setters sont respéctivement des accésseurs en lecture et en écriture.
get pour lire : accéder aux valeurs des variables d'instance
set pour alterer modifier les valeurs de variables d'instance

**Les constructeurs**
Un constructeur est une méthode spéciale utilisée pour initialiser des objets. Le constructeurr est appelé lorsqu'un objet d'une class est créé. Il peut être utilisé pour définir les valeurs initiales des attributs d'objet:
Notez que le nom du constructeur doit correspondre au nom de la class. Toutes les class ont des constructeurs par défaut: si vous ne créez pas vous-même de constructeur de class, Java en crée un pour vous. Cependant, vous ne pouvez pas définir de valeurs initiales pour les attributs d'objet.

**Une Variable d´instance**
c´est une variable qui est specifique a un objet, on ne peut l´utiliser que sur un objet.
```
Public Class Personne {
  private Sring nom;
  private int age;
```

**Une variable de class** 
Une variable de class n´est creer qu´une seule fois et sera partage par l'ensemble des objets. Cela peut etre utile pour récuperer le nombre d´objet creer par exemple.
```
Public Class Personne {
  public static int nombreTotalDePersonnes = 0;
 
```
Il faut imperativement l´appeler par sa classe et non par l´objet
```
System.our.println(Personne.nombreTotalDePersonnes);
```
**Une variable constante**
Une variable constante est une variable dont la valeur ne peut etre modifiée.

**Les Exceptions**
Java utilise des exceptions pour traiter les événements pouvant survenir lors de certaines opérations. Lorsque l’on utilise de telles opérations il est impératif de prendre en compte la récupération et le traitement des éventuelles exceptions.

**Le transtypage et le polymorphisme**
Le transtypage (conversion de type ou **cast en anglais**) consiste à modifier le type d'une variable ou d'une expression. 
Il existe deux types de transtypages: **le transtypage implicite** et **le transtypage explicite**.
Il est possible de convertir un objet d'une classe en un objet d'une autre classe si les classes ont un lien d'héritage (encore une fois, on utilise le mot objet par abus de langage : ce sont les références aux objets et non les objets eux-mêmes qui sont transtypés). Le transtypage d'un objet dans le sens fille -> mère est implicite.
En revanche, le transtypage dans le sens mère -> fille doit être explicite et n'est pas toujours possible.

**Java ArrayList ou Collections d'Objets**
En Java la taille d'un tableau ne peut pas être modifiée d'où l'importance du arrayList : les éléments peuvent être ajoutés et supprimés à tout moment. La syntaxe est également légèrement différente:
```
import java.util.ArrayList; // import the ArrayList class

List<Car> cars = new ArrayList<>(); // Create an ArrayList object
```
`add()` //permet d'ajouter un élément ;`get(int index)` //retourne l'élément à l'indice demandé ;`remove(int index)` //efface l'entrée à l'indice demandé ;`isEmpty()`// renvoie « vrai » si l'objet est vide ;`removeAll()` //efface tout le contenu de l'objet ;`contains(Object element)` //retourne « vrai » si l'élément passé en paramètre est dans l'ArrayList;`.size()` //permets de connaitre la longuer de l'arrayList comme .length dans d'autres languages.

### 2_L'Oblet Vs Le Procédural

Dans un programme traditionnel orienté procédure, vous commencez le processus par le haut, avec le programme principal.
Dans la programmation orientée objet, il n'y a pas de "top". Vous trouvez d'abord les classes, puis vous ajoutez des méthodes à chaque classe. (Une règle empirique simple pour identifier les classes consiste à rechercher les noms dans l'analyse du problème. Les méthodes, en revanche, correspondent à des verbes).

Dans la programmation orientée objet, les structures de données passent en premier, les algorithmes passent en second.
