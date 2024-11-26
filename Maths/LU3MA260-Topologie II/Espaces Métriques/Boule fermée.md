#topo
## Définition
Soit un espace métrique $(X, d)$, avec $x \in X$ et $\alpha > 0$.
On appelle la boule fermée de centre $x$ et de rayon $\alpha$, l'ensemble: #!

$$B_f(x, \alpha) = \set{y \in X, d(x,y) \leq \alpha}$$
<!--ID: 1729504947035-->



## Convergence des [[Travaux sur les suites|suites]] dans un [[Notions de fermé, adhérence et frontière|fermé]]
On observe le phénomène suivant: #!

$E \subseteq X$ est un fermé, si et seulement si, toute suite $(x_n)_{n \in \mathbb N} \in E^\mathbb N$ converge dans $E$
<!--ID: 1729504947038-->



### Preuve
$\Rightarrow$: 
Soit $E$ un fermé, on pose une suite $(x_n)_{n \in \mathbb N}$ une suite de $E$ qui converge vers $x \in X$
On a déjà que $x \in \overline{E}$, et comme $E$ est un fermé $\overline{E} = E$

$\Leftarrow$:
On va montrer que $E = \overline{E}$
On a déjà que $E \subseteq \overline{E}$, donc montrons que $\overline{E} \subseteq E$

Soit $x \in \overline{E}$, d'après la [[Travaux sur les suites#Caractérisation séquentielle de l' Notions de fermé, adhérence et frontière Définition de l'adhérence adhérence|caractérisation séquentielle de l'adhérence]] on a $(x_n)_{n \in \mathbb N}$ une suite de $E$ qui converge vers $x$.
Or on a supposé qu'une suite convergente de $E$ converge vers un élément de $E$. Donc $x \in E$
$$\tag*{$\blacksquare$}$$