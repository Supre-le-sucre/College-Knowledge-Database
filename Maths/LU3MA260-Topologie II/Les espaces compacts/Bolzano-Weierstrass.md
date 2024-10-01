## Théorème de Bolzano-Weierstrass
On énonce le théorème sur la compacité suivant: #!

$$\forall a < b, [a,b] \text{ est un compact}$$

### Preuve
Soit $(x_n)_{n \in \mathbb N}$ une suite dans $[a,b]$ montrons qu'il existe une sous-suite convergente dans $[a,b]$.

On rappelle que si $A \subset \mathbb R$ est un ensemble borné, alors il admet une borne supérieur $M$
$$\forall x \in A, x \leq M$$
$$\forall \epsilon > 0, \exists x  \in A, x \leq M-\epsilon$$

On considère la suite $y_n = \sup_{k \leq n}\set{x_k}$
Elle est décroissante, en effet, si on considère $A_n = \set{x_k, k \geq n}$ alors $A_{n+1} \subseteq A_n$. L'ensemble Et si $x \in A_n, x \leq M$ on a aussi $x \in A_{n+1}, x \leq M$

Or comme $y_n$ est une suite de $[a,b]$, elle est donc minorée, donc elle converge vers un élément $L$.
