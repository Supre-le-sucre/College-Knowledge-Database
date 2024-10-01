## Définition
Soit $(X,d)$. Une famille de partie de $X$ est qualifiée de recouvrement si et seulement si: #!
l'union de ces parties est égale à $X$

## Propriété, recouvrement d'un compact
On observe que l'on peut recouvrir un compact de la façon suivante: #!

$(X, d)$ est un compact, alors
$$\forall \epsilon > 0, \exists(x_1, \dots, x_N), X = \bigcup_{i=1}^NB(x_i, \epsilon)$$
==La réciproque est fausse==: $X=]0,1[$

### Preuve
On raisonne par contraposée.
$$\exists \epsilon > 0, \forall n \in \mathbb N^*, \forall(x_1, \dots x_N), \bigcup_{i=1}^NB(x_i, \epsilon) \subset X$$
On aimerait montrer que $X$ n'est pas compact
On va extraire construire $(x_n)$ qui n'admet aucune sous-suite qui sera convergente
$x_0 \in X$ et $B(x_0, \epsilon) \subset X$
Et $\exists x_1$ tel que $d(x_1, x_0) \geq \epsilon$ $B(x_1, \epsilon) \cup B(x_0, \epsilon) \subset X$
On raisonne par récurrence...  Donc finalement $\forall p \not = q, d(x_p, x_q) \geq \epsilon$, donc $(x_n)$ n'est pas de Cauchy, donc on ne peut pas extraire de sous-suite convergente.


## Théorème sur la compacité et complétude par recouvrement

