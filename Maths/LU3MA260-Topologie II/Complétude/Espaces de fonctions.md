## Complétude des espaces de fonctions
En posant $(X, d_x)$ et $(Y, d_y)$, deux espaces métriques complets, on observe que ces espaces sont complet: #!

- $(\mathcal B (X, Y), d_\infty)$ où $\mathcal B(X, Y)$ représente les fonctions de $X$ vers $Y$ bornées
- Les sous-espaces continues bornées, munies de la distance $d_\infty$ sont aussi complet
Rappelons que l'on pose: $$d_\infty(f,g) = \sup_{x \in X}d_Y(f(x), g(x))$$
### Preuve

1)
Pour ne pas avoir de notations trop lourde, posons l'[[Espaces complet#Espace de Banach|espace de Banach]] $(Y, ||\cdot||_Y)$
On alors $||f||_\infty = \sup_{x \in X}||f(x)||_Y$ la norme associée à $d_\infty$

On considère $(f_n)_{n\in \mathbb N}$ une suite de Cauchy dans $\mathcal B(X, Y)$, montrons donc qu'elle converge

Observons dans un premier temps que
$$\forall \epsilon> 0, \exists N \in \mathbb N, \forall n, p \geq N, \forall x \in X, ||f_n(x) - f_p(x)||_Y \leq \epsilon$$
Donc la suite $\forall x \in X$, la suite $(f_n(x))_{n \in \mathbb N}$ dans $Y$ est de Cauchy. Or $(Y, ||\cdot||_Y)$ est un espace complet. Donc cette suite converge vers un élément $f(x)$
Montrons alors que $f_n$ converge uniformément vers $f$

Comme $(f_n)$ est une suite de Cauchy
$$\forall \epsilon> 0, \exists N \in \mathbb N, \forall n, p \geq N, \forall x \in X, ||f_n(x) - f_p(x)||_\infty \leq \epsilon$$
Et par passage à la limite sur $p$:
$$\forall \epsilon> 0, \exists N \in \mathbb N, \forall n, p \geq N, \forall x \in X, ||f_n(x) - f(x)||_\infty \leq \epsilon$$

