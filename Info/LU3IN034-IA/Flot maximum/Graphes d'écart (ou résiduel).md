## Capacité résiduelle
On définit la capacité résiduel d'un [[Graphes de capacité]] comme: #!

$$r(u,v) = c(u,v)-f(u,v)$$
Avec $f$ le [[Flots]]
<!--ID: 1726076885840-->


## Graphe d'écart ou résiduel
Le graphe d'écart de $G = (V, E, c)$ est le graphe décrit par: #!
$$G_f = (V, E_f, r) \;\;\; E_f = \set{\set{u,v} \in E\; |\; r(u,v) > 0}$$
où $r$ est la [[#Capacité résiduelle]]
On observe que $|E_f| \leq 2 |E|$
**ATTENTION**: Le graphe d'écart possède aussi des arcs ==qui ne sont pas dans le graphe de départ !== On n'oublie pas la caractérisation antisymétrique du flot, en effet un sommet qui reçoit renverra ce qu'il reçoit au sommet qui lui donne dans le graphe résiduel
<!--ID: 1726076885850-->

#### Exemple
![[Pasted image 20241026191436.png]]

## Lemmes des flots dans un graphe d'écart
On qualifie la $f'$ une fonction de flot dans $G_f$ et $f$ une fonction de flot dans $G$. On observe alors que

i) $f'$ est un flot de $G_f$ si et seulement si la fonction $f + f'$ est une fonction de flot dans $G$
ii) $|f'|$ est un [[Flots#Définition|flot maximum]] dans $G_f$ si et seulement 

# Choisir le Chemin augmentant

## Définition
Un chemin augmentant est #!
Est un chemin entre $s$ et $t$ dans le graphe d'écart. En d'autres termes, le chemin augmentant permet de constater si le graphe ne peut pas recevoir du flot supplémentaire
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

