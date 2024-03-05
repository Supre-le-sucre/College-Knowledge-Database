#probas 

## Définition
Soient $A$ et $B$ deux événements d'un [[Espaces probabilisés]] $(\Omega, \mathcal F, \mathbb P)$ avec $\mathbb P(B) > 0$.
On définit la probabilité conditionnelle de $A$ sachant B la quantité: #!
$$\mathbb P(A | B) = \frac{\mathbb P(A \cap B)}{\mathbb P(B)}$$
<!--ID: 1709675798888-->


## Probabilité conditionnelle en chaîne
Soient $n \geq 2$ et $A_1, \dots, A_n$, des événements tels que $\mathbb P\left(\bigcap_{i=1}^{n-1}A_i\right) > 0$
Alors on peut poser pour $\mathbb P\left(\bigcap^n_{i=1}A_i\right)$... #!
$$\mathbb P\left(\bigcap^n_{i=1}A_i\right) = \mathbb P(A_1)\mathbb P(A_2 | A_1)\mathbb P(A_3 | A_1 \cap A_2) \cdots \mathbb P(A_n|A_1 \cap \cdots \cap A_n)$$
$$ = \mathbb P(A_1) \prod_{i=2}^n\mathbb P\left(A_i | \bigcap_{k=1}^{i-1}A_k\right) $$
<!--ID: 1709675798898-->


## Formules de décompositions fondamentales
### Partitionnement
Soit un [[Espaces probabilisés]] $(\Omega, \mathcal F, \mathbb P)$ un espace probabilisé, et soit $(B_i)_{i \in I}$ une partition dénombrable de $\Omega$ (i.e $B_i \cap B_j = \emptyset, \forall i\not=j$ et $\bigcup_{i \in I} B_i = \Omega$)
Pour un événement $A$ on peut décomposer $\mathbb P(A)$ tel que: #!
$$\mathbb P(A) = \sum_{i \in I} \mathbb P(A \cap B_i)$$
<!--ID: 1709675798904-->


### Probabilités totales
On définit, de plus, pour $(B_i)_{i \in I}$ une partition dénombrable de $\Omega$ tel que $\mathbb P(B_i) > 0, \forall i \in I$ une décomposition de $\mathbb P(A)$ telle que: #!
$$\mathbb P(A) = \sum_{i \in I}\mathbb P(A |B_i) \mathbb P(B_i)$$
<!--ID: 1709675798910-->

