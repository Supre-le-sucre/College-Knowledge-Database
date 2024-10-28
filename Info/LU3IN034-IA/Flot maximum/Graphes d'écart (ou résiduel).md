## Capacité résiduelle
On définit la capacité résiduel d'un [[Graphes de capacité]] comme: #!

$$r(u,v) = c(u,v)-f(u,v)$$
Avec $f$ le [[Flots]]
<!--ID: 1730114115943-->



## Graphe d'écart ou résiduel
Le graphe d'écart de $G = (V, E, c)$ selon le flot $f$ est le graphe décrit par: #!
$$G_f = (V, E_f, r) \;\;\; E_f = \set{\set{u,v} \in E\; |\; r(u,v) > 0}$$
où $r$ est la [[#Capacité résiduelle]]
On observe que $|E_f| \leq 2 |E|$
**ATTENTION**: Le graphe d'écart possède aussi des arcs ==qui ne sont pas dans le graphe de départ !== On n'oublie pas la caractérisation antisymétrique du flot, en effet un sommet qui reçoit renverra ce qu'il reçoit au sommet qui lui donne dans le graphe résiduel
<!--ID: 1730114115945-->


#### Exemple
![[Pasted image 20241026191436.png]]

## Lemmes des flots dans un graphe d'écart
On qualifie la $f'$ une fonction de flot dans $G_f$ et $f$ une fonction de flot dans $G$. On observe alors que: #!

i) $f'$ est un flot de $G_f$ si et seulement si la fonction $f + f'$ est une fonction de flot dans $G$
ii) $f'$ est un [[Flots#Définition du flot maximum|flot maximum]] dans $G_f$ si et seulement si $f + f'$ est un flot maximum de $G$
iii) $|f \pm f'| = |f| \pm |f'|$
iv) Soit $f^*$ un flot maximum de $G$, alors la valeur du flot max dans $G_f$ est égale à $|f^*| -|f|$
<!--ID: 1730114115947-->


# Chemin augmentant

## Définition de chemin augmentant
Un chemin augmentant est #!
Est un chemin entre $s$ et $t$ dans le graphe d'écart. En d'autres termes, le chemin augmentant permet de constater si le graphe ne peut pas recevoir du flot supplémentaire
<!--ID: 1730114115949-->


## Capacité résiduel d'un chemin
La capacité résiduel d'un chemin $p$ dans le graphe résiduel $G_f$... 
La capacité résiduel ==minimale== de ses arcs.

## Chemin de capacité critique
On qualifie le chemin de capacité critique: #!
Celui dont la capacité résiduelle est maximum.
<!--ID: 1730114115950-->


## Propriété sur le chemin de capacité critique
On observe la propriété suivante: #!

Dans un graphe $G = (V, E, c)$ de flot maximum $F$, la capacité résiduel du chemin critique est d'au moins $\frac{F}{|E|}$
<!--ID: 1730114115952-->




