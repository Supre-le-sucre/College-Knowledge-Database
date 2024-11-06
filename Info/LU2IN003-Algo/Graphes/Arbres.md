#algo
## Définition
On définit un arbre (en tant que graphe) comme: #!
Un [[Graphes non orientés]] [[Graphes non orientés#Connexité|connexe]] acyclique (i.e sans [[Graphes non orientés#Cycles|Cycle]])
<!--ID: 1715702538633-->


## Théorème
Soit $T = (V, E)$ un [[Graphes non orientés]], alors les assertions suivantes sont équivalentes pour définir un arbre: #!
- T est un arbre
- T est [[Graphes non orientés#Minimal connexe|minimal connexe]]
- T est [[Graphes non orientés#Maximal acyclique|maximal acyclique]]
- Entre deux sommets quelconques, il existe une [[Graphes non orientés#Chaîne|chaîne élémentaire]] unique.
<!--ID: 1715702538636-->


## Relation entre $E$ et $V$ pour la connexité et l'existence de cycles
On observe les phénomènes suivants: #!

Soit $G = (V, E)$ un [[Graphes non orientés]].
- Si $|E| \geq |V|$, alors on a que $G$ contient un [[Graphes non orientés#Cycles|cycle élémentaire]]
- Si $|E| < |V| - 1$, alors $G$ n'est pas [[Graphes non orientés#Connexité|connexe]]
<!--ID: 1715702538639-->


### Corollaire sur la relation entre $E$ et $V$ dans un arbre
On observe alors que: #!
$T$ est un arbre si et seulement si $|E| = |V| - 1$
<!--ID: 1715702538641-->
