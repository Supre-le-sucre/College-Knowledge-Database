## Capacité résiduelle
On définit la capacité résiduel d'un [[Graphes de capacité]] comme: #!

$$r(u,v) = c(u,v)-f(u,v)$$
Avec $f$ le [[Flots]]

## Graphe d'écart ou résiduel
Le graphe d'écart de $G = (V, E, c)$ est le graphe décrit par: #!
$$G_f = (V, E_f, r) \;\;\; E_f = \set{\set{u,v}\; |\; r(u,v) > 0}$$
où $r$ est la [[#Capacité résiduelle]]
On observe que $|E_f| \leq 2 |E|$
