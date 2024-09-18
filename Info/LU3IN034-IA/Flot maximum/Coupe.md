
## Définition d'une coupe
On dit que $(A, B)$ est une coupe pour $G = (V, E, c, s, t)$ un [[Graphes de capacité]] si: #!

$A, B$ sont des partitions de $V$ et tel que $s \in A$ et $t \in B$
<!--ID: 1726076885908-->


### Capacité d'une coupe
On définit la capacité de la coupe $(A, B)$: #!
$$c(A, B) = \sum_{u \in A, v \in B} c(u, v)$$
### Flot d'une coupe
On définit le [[Flots|flot]] d'une coupe $(A,B)$: #!
$$f(A, B) = \sum_{u \in A, v \in B} f(u,v)$$
<!--ID: 1726076885917-->


## Comment trouver une coupe minimale ?
On effectue l'algorithme suivant: #!

a) Commencer par le [[Graphes d'écart (ou résiduel)]] final $G_{f^*}$ (avec [[Flots]] maximum)
b) On détermine l'ensemble de sommets que l'ont peut atteindre dans $G_{f^*}$ en commençant par la source $s$, appelons le A
c) Soit $B = V \setminus A$
d) Une coupe minimale serai donc $(A, B)$
<!--ID: 1726076885926-->
