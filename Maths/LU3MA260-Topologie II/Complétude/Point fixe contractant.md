## Définition contractant
Soit $(X, d)$ un espace métrique avec $f: X \to X$. On dit qu'elle est $k$-contractante si et seulement si: #!
$$\forall (x,y) \in X^2, d(f(x), f(y)) \leq kd(x,y)$$

## Définition point fixe
Pour une fonction $f$ on appelle point fixe, un élément $x \in X$ tel que: #!
$$f(x) = x$$

## Théorème du point fixe de Picard
On énonce le théorème suivant: #!

Soit $(X,d)$ un espace métrique complet et soit $f: X \to X$ une fonction $k$-contractante avec $(k < 1)$.
Alors il existe un unique point fixe à $f$.
De plus $\forall x_0 \in X$, la suite récurrente définie par $x_{n+1} = f(x_n)$ converge vers cet unique point fixe

### Preuve

On va montrer que ce point fixe existe en construisant la suite récurrente $(x_n)_{n \in \mathbb N}$ définie telle que $x_0 \in X$ et $x_{n+1} = f(x_n)$

1)
Montrons d'abord que si $x_n \to x$, alors $x$ est un point fixe
Supposons donc que la suite converge, on a alors que
$\lim_{n \to +\infty} x_n =x$ et $\lim_{n \to +\infty} x_{n+1} =x$ par unicité de la limite.

Ainsi donc par passage à la limite, on a que $x_{n+1}= f(x_n)$ devient $x =f(x)$

2)
Montrons ensuite que le point fixe est unique

Pour cela, on pose $(x_1, x_2) \in X^2$ tel que $f(x_1)=x_1$, $f(x_2)=x_2$
Comme $f$ est $k$-contractante on a que

$$d(f(x_1), f(x_2)) \leq kd(x_1, x_2)$$
$$d(x_1, x_2) \leq kd(x_1, x_2)$$
$$(1-k)d(x_1, x_2) \leq 0$$
Donc comme $(1-k) > 0$ on a forcément que $d(x_1, x_2) = 0$ et donc par [[Notions d'ouvert par les distances#Définition d'une distance|séparation de la distance]] on a que $x_1 = x_2$

3)
Vérifions maintenant que $(x_n)$ converge bien
Pour cela, comme l'espace est complet, il suffit de montrer qu'elle est de Cauchy

$d(x_{n+1}, x_n) = d(f(x_n), f(x_{n-1})$
Or comme $f$ est $k$-contractante on a que
$$d(f(x_n), f(x_{n-1})) \leq k(x_n, x_{n-1})$$
$$d(x_{n+1}, x_n)) \leq k(f(x_{n-1}), f(x_{n-2}))$$

Donc en poursuivant par récurrence on a que
$$d(x_{n+1}, x_n)) \leq k^nd(x_1, x_0), \forall n \geq 1$$

Or observons que, par inégalité triangulaire de la distance
$$d(x_p, x_n) \leq d(x_p, x_{p-1}) + \cdots + d(x_{n+1}, x_{n})$$
$$d(x_p, x_n) \leq k^pd(x_1,x_0) + \cdots + k^nd(x_1,x_0)$$
$$d(x_p, x_n)$$