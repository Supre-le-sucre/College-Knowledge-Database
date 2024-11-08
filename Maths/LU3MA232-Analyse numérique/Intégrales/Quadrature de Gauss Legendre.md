## Méthode
On définit la méthode de Gauss-Legendre de la façon suivante: #!

En fixant $n \geq 1$ considérant les racines $y_{1}, \dots, y_{n}$ de $P_{n}$ avec $P_{n}$ un [[Polynôme de Legendre]].
On pose $$
\int_{-1}^1 f(y)dy \approx 2 \sum_{i=1}^{n}\lambda_{i}f(y_{i})  
$$
Avec des $\lambda_{i}$ choisit pour avoir une méthode d'ordre au moins $n-1$

## Théorème sur l'ordre de Gauss-Legendre
On observe que la méthode de Gauss-Legendre est telle que: #!

Lorsqu'elle est basée sur les racines de $P_{n}$ est d'ordre $2n-1$


### Preuve
Soit $M \in \mathbb{R}_{2n-1}[X]$. En faisant la division euclidienne de $M$ par $P_{n}$ on obtient
$$
M = QP_{n} + R
$$
Avec $Q$ et $R$ de degré $\leq n-1$.

En appliquant la méthode de Gauss Legendre, on observe que
$$
2 \sum_{i=1}^{n} \lambda_{i}M(y_{i}) = 2 \sum_{i=1}^{n} \lambda_{i}Q(y_{i})P_{n}(y_{i}) + 2 \sum_{{i=1}}^n\lambda_{i}R(y_{i}) $$

Or $P_{n}(y_{i}) = 0$ Donc $\sum_{i=1}^{n} \lambda_{i}Q(y_{i})P_{n}(y_{i}) = 0$
Et on sait aussi que les $\lambda_{i}$ ont été choisi pour rendre le schéma d'au moins $n-1$. Donc 
$$
2 \sum_{{i=1}}^n\lambda_{i}R(y_{i}) = \int _{-1}^1 R(y) \, dy 
$$
D'où 
$$
2 \sum_{i=1}^{n} \lambda_{i}M(y_{i}) = \int _{-1}^1 R(y) \, dy  
$$
d'une part.

Et d'autres part, en repartant de la division euclidienne
$$
\int_{-1}^1M(y)dy = \int_{-1}^1Q(y)P_{n}(y)dy + \int_{-1}^1R(y)dy
$$