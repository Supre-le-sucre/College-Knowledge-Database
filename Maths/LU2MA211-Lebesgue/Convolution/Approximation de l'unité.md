## Intérêt
On observe que le [[Produit de convolution]] n'admet aucun élément neutre dans $L^1(\mathbb R)$. L'objectif ici est de former une suite de fonction de $L^1(\mathbb R)$ afin d'approximer un élément neutre en l'infini.


## Définition
On définit une approximation de l'unité de la façon suivante: #!

Soit $\rho_k:\mathbb R \to \mathbb R^+$ une suite de fonctions mesurables positives est qualifiée d'approximation de l'unité lorsque: $$\int_\mathbb R \rho_k = 1$$ et aussi $$\forall\delta > 0, \lim_{k \to +\infty}\int_{[-\delta,\delta]}\rho_k = 1 \Leftrightarrow \forall\delta > 0, \lim_{k \to +\infty}\int_{\mathbb R\setminus[-\delta,\delta]}\rho_k = 0 $$ L'équivalence se déduisant par la relation de Chasles
<!--ID: 1714516791370-->


## Construction d'une approximation de l'unité
On peut construire une approximation de l'unité simplement de la façon suivante: #!

Si $\rho: \mathbb R \to \mathbb R^+$ est une fonction d'intégrale 1, alors la suite de fonction définie par $$\rho_k(x) = k\rho(kx)$$ est un approximation de l'unité
<!--ID: 1714516791372-->


## Théorème de convergence
Il est possible d'étudier ces convergence avec la convolution d'une approximation de l'unité $\rho_k$ et d'une fonction $f$: #!

- Si $f \in L^1(\mathbb R)$, alors la suite $(f*\rho_k)\to f$ dans $L^1(\mathbb R)$
- Si $f \in L^2(\mathbb R)$, alors la suite $(f*\rho_k)\to f$ dans $L^2(\mathbb R)$
- Si $f$ est bornée et uniformément continue alors la suite $(f*\rho_k)\to f$ converge uniformément.
<!--ID: 1714516791374-->
