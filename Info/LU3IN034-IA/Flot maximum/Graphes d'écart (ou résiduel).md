## Capacité résiduelle
On définit la capacité résiduel d'un [[Graphes de capacité]] comme: #!

$$r(u,v) = c(u,v)-f(u,v)$$
Avec $f$ le [[Flots]]
<!--ID: 1726076885840-->


## Graphe d'écart ou résiduel
Le graphe d'écart de $G = (V, E, c)$ est le graphe décrit par: #!
$$G_f = (V, E_f, r) \;\;\; E_f = \set{\set{u,v}\; |\; r(u,v) > 0}$$
où $r$ est la [[#Capacité résiduelle]]
On observe que $|E_f| \leq 2 |E|$
<!--ID: 1726076885850-->

# Choisir le Chemin augmentant

## Définition
Un chemin augmentant est #!
Un chemin dans un graphe d'écart tel que la capacité résiduel de chaque arc du chemin augmente.
<!--ID: 1727256183789-->


## Capacité résiduel d'un chemin
La capacité résiduel d'un chemin $p$ dans le graphe résiduel $G_f$... #! 
C'est la capacité résiduel minimale de ses arcs.
On qualifie le chemin de capacité critique, celui dont la capacité résiduelle au maximum.
<!--ID: 1727256183800-->


## Propriété sur le chemin critique
On observe la propriété suivante: #!

Dans un graphe $G = (V, E, c)$ de flot maximum $F$, la capacité résiduel du chemin critique est d'au moins $\frac{F}{|E|}$
<!--ID: 1727256183814-->


## Complexité de l'algorithme de selection de chemin
Pour sélectionner le bon chemin augmentant, on doit choisir le chemin critique.
Le nombre d'itérations de l'algorithme est de:  #!
$$O(|E| \log(F))$$
<!--ID: 1727256183829-->

