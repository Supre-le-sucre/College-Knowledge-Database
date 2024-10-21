## Propriété sur les bornes atteintes
On observe le phénomène suivant: #!

Soit $f: (X, d) \to \mathbb R$ continue et $X$ est un compact.
$$\implies \exists a \leq b \in \mathbb R, \forall x \in X, a \leq f(x) \leq b$$
Avec $f$ atteignant ses bornes: $f(x_0) = a$ et $f(x_1)= b$
<!--ID: 1729505040460-->


### Preuve

Soit $f$ continue et $X$ compact, alors $f(X)$ est un compact et on peut définir 
$a = \inf_{x \in X} f(x)$ et $b = \sup_{x \in X} f(x)$

Montrons alors que l'$\inf$ et le $\sup$ sont atteints.
Pour l'$\inf$, d'après la définition de $a$, on a $(x_n)_{n \in \mathbb N}$ $f(x_n) \to a$
Et comme $X$ est compact, il existe une sous-suite de $(x_n)$ convergente en $a$.
Comme $f$ est continue, cette sous-suite converge vers $x_0$

