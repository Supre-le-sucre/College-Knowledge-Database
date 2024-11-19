# Définition
Pour $E$ et $F$ deux espaces vectoriels. On dit que $f: E \to F$ est différentiable au point $a$ si et seulement si: #!

Il existe application linéaire $L_{a} \in \mathcal L(E, F)$ tel que $$
f(a+h) = f(a) + L_{a}(h) + o(h)
$$
On dit alors que $L_{a}$ est le différentielle de $f$ au point $a$ et on note souvent $L_{a} = D_{f}(a)$

## Exemple
### Générique

Pour $f(x, y) = xe^{3y}$ a-t-on $f$ différentiable au point $(2, 1)$
On évalue donc la fonction avec
$$f(2 + h_{1}, 1 + h_{2}) = (2+h_{1})e^{3(1+h_{2})} = (2+h_{1})e^3\times e^{3h_{2}}$$
En effectuant un développement limité d'exponentiel, alors on obtient
$$f(2+h_{1}, 1+h_{2}) = (2+h_{1})e^3 \times[1 + 3h_{2} + o(h_{2})]$$
En posant $h = (h_{1}, h_{2})$, On a $o(h_{1}h_{2}) = o(h)$
$$
f(2+h_{1}, 1+h_{2}) = 2e^3 +h_{1}e^3 + 6h_{2} e^3 + o(h)
$$
 En posant $D_{f}(a)(h) = h_{1}e^3 + 6h_{2}e^3$ on obtient bien
$$f(2+h_{1}, 1+h_{2}) = f(2, 1) + D_{f}(a)(h) + o(h)$$

### Matricielle
On s'intéresse cette fois à la différentielle de $f: H \in B(0, 1) \mapsto (I+H)^{-1}$

#### Montrons d'abords que $f$ est bien défini
On sait qu'en dimension 1:
$$
\frac{1}{(1+x)} = \sum_{k=0}^{+\infty}(-x)^k 
$$
Un bon candidat serait alors $A = \sum_{k=0}^{+\infty}(-H)^k$ et en plus de vouloir $A(I+H) = (I+H)A = I$ on veut aussi montrer que $A$ est bien défini.
Comme l'espace des matrices de dimension $n$ est complet (car fini et normé), il suffit alors de montrer que la suite $S_{n} = \sum_{k=0}^{n}(-H)^k$ est de Cauchy et nous aurons montrer sa convergence (i.e $A$ sera bien défini)

Or pour $p > n$
$$
||S_{p} -S_{n}|| = \left| \left| \sum_{k=n}^{p}(-H)^k  \right|  \right| \leq \sum_{k=n}^{p} ||H||^k 
$$
Et comme $H \in B(0, 1)$ et que
$$
\sum_{k=n}^{p} ||H||^k  \leq \sum_{k=n}^{+\infty}||H||^k 
$$
Comme $\sum_{k=n}^{+\infty}||H||^k \to 0$ lorsque $n$ tends vers l'infini (reste d'une série convergente)
On a bien que $||S_{p} -S_{n}|| \to 0$ lorsque $n$ tends vers $+\infty$, et donc la suite est bien de Cauchy.
Donc $A$ est bien définie.

De plus
$$
A(I+H) = \lim_{  n \to \infty } S_{n}\circ(I+H) =  \lim_{ n \to \infty } \sum_{k=0}^{n} (-H)^k(I+H) = \lim_{ n \to \infty } H^{n+1}(-1)^n + I = I
$$
Car en effet $$\sum_{k=0}^{n} (-H)^k(I+H) = \sum_{k=0}^{n}(-H)^k + \sum_{k=0}^{n}(-H)^{k} \times H $$
On obtient une série télescopique.
Le même résultat a lieu dans l'autre sens.

#### Montrons ensuite qu'elle est differentiable

### Espaces de fonctions
En posant l'espace $E = \mathcal C([0, 1], \mathbb{R}), ||\cdot||_{\infty}$
Et $g: E \to E$ avec $g: f \mapsto f\times f = f^2$

On pose alors $$
g(f+h) = (f+h)^2 = f^2 + 2fh + h^2 = g(f) + 2fh + o(h)
$$

Un candidat pour $L_{f}(h)$ est alors $2fh$. On a bien que $L_{f}$ est linéaire dans l'espace de fonction considéré. En revanche il y a ambiguïté sur sa continuité. Mais elle est bien continue

$$
||L_{f}(h)||_{\infty} = ||2fh||_{\infty} \leq ||2 f||_{\infty}||h||_{\infty} < + \infty
$$
Car $f$ et $h$ sont continues.

## Proposition sur la continuité
On observe que: #!

Les fonctions $f: \Omega \to F$ et $a \in \Omega$ tel que $f$ différentiable au point $a$, alors elle est aussi continue au point $a$

### Preuve
Il suffit de faire tendre $h$ vers $0$ dans la formule de différentiabilité de $f$ en $a$.
Comme $L_{a}(h)$ est linéaire, si $h$ tends vers $0$ alors lui aussi. D'où la continuité en $a$

## Définition
On dit que $f$ est différentiable si et seulement si: #!

Elle est différentiable en tout point de son espace de définition.

## Propriété sur les opérations