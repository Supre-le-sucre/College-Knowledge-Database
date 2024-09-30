# Définition
On définit un problème linéaire d'optimisation de la façon suivante: #!

Un problème linéaire est un problèmes ayant un ensemble de contraintes linéaires (égalité ou inégalité). Et dont la fonction objective d'un tel problème peuvent être le maximum ou le minimum d'une application linéaire.
<!--ID: 1727256183774-->


## Représentation géométrique
Les problèmes linéaire d'optimisation peuvent se représenter géométriquement, en particulier s'il n'y a pas plus de 3 variables.
Chaque variable représente un axe, et les contraintes définissent l'ensemble d'étude: en faisant l'intersection de tous les espaces contraints.

En règle générale, l'optimum se trouve dans un des sommets de la région réalisables.

### Determination d'un sommets de manière algébrique
Les sommets de notre ensemble d'étude sont: #!
les contraintes d'inégalité transformée en égalités. Pour établir cela, il nous faut des variables d'écart, qui seront à 0 à un sommet. 
<!--ID: 1727686902314-->


On pose alors les variables d'écart: #!
Les variables qui complètes les variables de notre problèmes pour transformer les inégalités de notre problème en égalité. ==Il n'y a pas de variable d'écart à placer dans la fonction objectif== 
La valeur des variables d'écart donnerons la valeurs des variables dans notre problème.
<!--ID: 1727686902333-->


**Remarque**: Observons qu'à chaque sommet, il y autant de variables (d'écart ou non) à 0 que de dimensions dans notre problème

#### Algorithme Simplexe
L'algorithme simplexe consiste à explorer l'ensemble des sommets de l'ensemble d'étude.
Pour se faire:
- On commence par un sommet quelconque
- On évalue s'il s'agit du maximum: on regarde si une des variables du problème à un rapport d'augmentation plus important (i.e: un coefficient dans la fonction objectif plus conséquent)
- On évalue ensuite les rapports des variables ne valant pas 0 (variables basiques).Le rapport de la variable $b$ sachant que $x$ est la variable du problème ayant le plus grand coefficient dans la fonction objectif est calculé par 
	(Valeur max de la variable $b$ autorisée) / (Coefficient de $x$ dans l'équation)
- On repère le rapport d'écart minimum et on passe la variable d'écart à 0 on change notre objectif en prenant compte de la nouvelle valeur maximale et en changeant les coefficient des variables convenablement.

## Exceptions aux PL
Si la région de résolution représente une intersection vide, alors le problèmes est irréalisable.
DE même si l'espace de résolution n'est pas majoré dans le cas d'une maximisation, ou minoré dans le cas du minimisation, alors le problème est irréalisable.