## Théorème de Bolzano-Weierstrass
On énonce le théorème sur la compacité suivant: #!

$$\forall a < b, [a,b] \text{ est un compact}$$

### Preuve
Soit $(x_n)_{n \in \mathbb N}$ une suite dans $[a,b]$ montrons qu'il existe une sous-suite convergente dans $[a,b]$.

On rappelle que si $A \subset \mathbb R$ est un ensemble borné, alors il admet une borne supérieur $M$
$$\forall x \in A, x \leq M$$
$$\forall \epsilon > 0, \exists x  \in A, x \leq M-\epsilon$$

On considère la suite $y_n = \sup_{k \leq n}\set{x_k}$