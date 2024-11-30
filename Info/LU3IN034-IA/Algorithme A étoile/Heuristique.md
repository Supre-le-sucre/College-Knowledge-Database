## Définition
Soit $h: N \to \mathbb{R}$ une fonction heuristique qui pour un état $n$ renvoie une valeur

- L'heuristique est monotone si et seulement si
$$
\forall n \in N, \forall m \in S(n), \quad h(n)-h(m) \leq k(n, m)
$$
- L'heuristique est coïncidente si et seulement si
$$
\forall \gamma \in \Gamma, \quad h(\gamma) = 0
$$
- L'heuristique est minorante si et seulement si
$$
\forall n \in N, \quad h(n) \leq h^{*}(n)
$$
- Une heuristique $h'$ est mieux informée que $h$ si et seulement si
$$
 \forall n \in N, \quad h(n) < h'(n) \leq h^{*}(n)
$$

## Proposition
Un heuristique monotone et coïncidente est forcément minorante

