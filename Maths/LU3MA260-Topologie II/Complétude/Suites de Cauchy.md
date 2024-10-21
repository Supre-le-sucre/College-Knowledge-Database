## Définition
Soit un espace métrique $(X, d)$ et une suite $(x_n)_{n \in \mathbb N} \in X^\mathbb N$. On dit que $(x_n)$ est de Cauchy si et seulement si: #!

$$\forall \epsilon > 0, \exists N \in \mathbb N, \forall p,q \geq N, d(x_p, x_q) \leq \epsilon$$
<!--ID: 1729504820714-->



## Lemme sur la convergence et les suites de Cauchy
On observe 2 propriétés fondamentales sur les suites de Cauchy: #!

- Toute suite convergente est de Cauchy
- Toute suite de Cauchy est bornée
<!--ID: 1729504820716-->



### Preuve
1)
Soit $(x_n)_{n \in \mathbb N}$ une suite de $X$ qui converge vers $x \in X$
$$\forall \epsilon > 0, \exists N \in \mathbb N, \forall n > N, d(x_n, x) < \epsilon$$

Observons que par [[Notions d'ouvert par les distances#Définition d'une distance|inégalité triangulaire des distances]]
$$d(x_p, x_q) \leq d(x_p, x) + d(x, x_q)$$
Donc $\forall p,q \geq N$ on a bien
$$d(x_p, x_q) \leq \epsilon$$

2)
Prenons $\epsilon = 1$ et observons qu'il existe $N$ tel que $\forall n \geq N, d(x_n, x_N) < 1$
Donc il suffit de prendre $M = \max{(\sup_{i \in [0, N] d(x_i, x_N)}, 1)}$ et on a bien 
$$\forall n \in \mathbb N, d(x_n, x_N) \leq M$$
$$\tag*{$\blacksquare$}$$
