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
Un chemin augmentant est un chemin dans un graphe d'écart tel que la capacité résiduel de chaque arc du chemin augmente.

## Capacité résiduel d'un chemin
La capacité résiduel d'un chemin $p$ dans le graphe résiduel $G_f$ est la capacité résiduel minimale de ses arcs.
On qualifie le chemin de capacité critique, celui dont la capacité résiduelle au maximum.