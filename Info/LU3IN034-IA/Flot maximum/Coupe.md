## Définition d'une coupe
On dit que $(A, B)$ est une coupe pour $G = (V, E, c, s, t)$ un [[Graphes de capacité]] si: #!

$A, B$ sont des partitions de $V$ et tel que $s \in A$ et $t \in B$
<!--ID: 1730114115928-->



### Capacité d'une coupe
On définit la capacité de la coupe $(A, B)$: #!
$$c(A, B) = \sum_{u \in A, v \in B} c(u, v)$$
Autrement dit, il s'agit de la somme des capacités des arcs connectant la partie A et B de la coupe.
<!--ID: 1730114115930-->


### Flot d'une coupe
On définit le [[Flots|flot]] d'une coupe $(A,B)$: #!
$$f(A, B) = \sum_{u \in A, v \in B} f(u,v)$$
Autrement dit, il s'agit de la somme des flots des arcs connectant la partie A et B de la coupe.
<!--ID: 1730114115932-->


