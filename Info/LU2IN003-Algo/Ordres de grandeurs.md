#algo 
cf. [[La notation de Landau]] pour les définitions
## Exemples de preuve de notation de Landau
- $5n+3 \in O(n^2)$
Si $n \geq 3, 5n +3 \leq 6n \leq 6n^2$
Si on pose $D=6$ et $n_0=3$
Alors $\forall n \geq n_0, 5n+3 \leq Dn^2$, donc $5n+3 \in O(n^2)$

- $5n+3 \in \Theta(n)$
Si on pose $D=6$ et $n_0=3$
Alors $\forall n \geq n_0, 5n+3 \leq Dn$

De plus, $n \in O(5n+3)$ car $D=1, n_0=1$
$\forall n \geq 1, n \leq 5n+3$
Finalement donc, $5n+3 = \Theta(n)$

- $5n+3 \in \Omega(1)$
On montre finalement $1 \in O(5n+3)$
Si $n_0 =1, D=1, \forall n \geq 1, 1 \leq 5n+3$
Ainsi donc $5n+3 \in \Omega(1)$


## Critères importants
- si $\lim_{n \to +\infty} \frac{f(n)}{g(n)} = 0$ alors $f\in O(g)$ et $f \not \in \Omega(g)$
- si $\lim_{n \to +\infty} \frac{f(n)}{g(n)} = +\infty$ alors $f\in \Omega(g)$ et $f \not \in O(g)$
-  si $\lim_{n \to +\infty} \frac{f(n)}{g(n)} = a$ alors $f\in \Theta(g)$
- 