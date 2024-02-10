#probas 
Dans la [[Théorie des ensembles]], on définit une famille arbitraire de sous-ensemble de $\Omega$, l'élément $(A_i)_{i\in I}$
On peut aussi nommer cet élément, comme une famille indexée par $I$ de sous ensemble $\Omega$.

**Remarque**: L'élément $(A_i)_{i\in I}$ représente aussi l'ensemble des fonctions de $I$ vers $\mathcal{P}(\Omega)$

## Unions et Intersections
Une famille arbitraire de sous-ensemble $(A_i)_{i\in I}$ respecte les notions d'union et d'intersection, et sont définit comme suit: #!
$$\bigcup_{i\in I}A_i := \set{\omega \in \Omega/ \exists i \in I, \omega \in A_i}$$
$$\bigcap_{i\in I}A_i := \set{\omega \in \Omega/ \forall i \in I, \omega \in A_i}$$
<!--ID: 1707587521201-->


### Complémentarité par définition
Il est naturel alors de comprendre le complémentaire de ces ensembles, en niant la définition:

Le complémentaire de l'union d'une famille de sous-ensemble est: #!
$$\overline{\bigcup_{i\in I}A_i} = \bigcap_{i\in I}\overline{A_i}$$
Puisque la négation de $\exists i \in I, \omega \in A_i$ se traduit par $\forall i \in I, \omega \not \in A_i$, où $\omega \not \in A_i := \omega \in \overline{A_i}$
La négation est alors la définition de l'intersection vue plus haut.
<!--ID: 1707587366054-->



De la même manière, on en déduit aussi que le complémentaire de l'intersection d'une famille de sous-ensemble est: #!
$$\overline{\bigcap_{i\in I}A_i} = \bigcup_{i\in I}\overline{A_i}$$
Puisque la négation de $\forall i \in I, \omega \in A_i$ se traduit par $\exists i \in I, \omega \not \in A_i$, où $\omega \not \in A_i := \omega \in \overline{A_i}$
La négation est alors la définition de l'union vue plus haut.
<!--ID: 1707587321506-->


### Distributivité
Une telle famille de sous ensemble respecte aussi toutes les lois de distributivités établies pour les ensembles. Définissons $C \subseteq \Omega$, on a alors: #!
$$\left(\bigcup_{i\in I}A_i\right)\cap C = \bigcup_{i\in I}(A_i \cap C)$$
$$\left(\bigcap_{i\in I}A_i\right)\cup C = \bigcap_{i\in I}(A_i \cup C)$$
<!--ID: 1707587335522-->



