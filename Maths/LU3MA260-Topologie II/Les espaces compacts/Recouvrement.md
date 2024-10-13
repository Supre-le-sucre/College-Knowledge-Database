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


## Théorème de Borel-Lebesgue
On énonce le théorème suivant: #!

Un espace $(X,d)$ est compact si et seulement si on peut en extraire un recouvrement fini. 

### Preuve
On montre d'abord le lemme suivant

#### Lemme
Soit un espace compact $(X, d)$ avec le recouvrement $X = \bigcup_{i \in \Lambda}O_i$ avec $O_i$ un ouvert.
Alors $$\exists \alpha > 0, \forall x \in X, \exists i \in \Lambda, B(x, \alpha) \subset O_i$$
##### Preuve du Lemme
On raisonne par l'absurde, supposons alors le recouvrement de $X = \bigcup_{i \in \Lambda}O_i$ et que
$$\forall \alpha > 0, \exists x \in X, \forall i \in \Lambda, B(x, \alpha) \not \subset O_i$$

Posons $\alpha_n = \frac{1}{n}$, alors on a $x_n \in X$ tel que $\forall i \in \Lambda, B(x_n, \alpha_n) \not \subset O_i$
Comme $(X, d)$ est un espace compact, alors on a $\phi$ tel que $x_{\phi(n)} \to x$ avec $x \in X$
On va montrer que $\forall i \in \Lambda, x \not \in O_i$, donc on aura $x \not \in \bigcup_{i \in \Lambda}O_i = X$ ce qui est absurde.

Comme $x \in X$, donc $\exists j \in \Lambda, x \in O_j$
Comme $O_j$ est un ouvert, alors $\exists \epsilon, B(x, \epsilon) \subset O_j$

Or on sait aussi que $\forall n \in \mathbb N$, $B(x_{\phi(n)}, \frac{1}{\phi(n)}) \not \in O_j$
On extrait $y_{\phi(n)} \in B(x_{\phi(n)}, \frac{1}{\phi(n)})$ donc $y_{\phi(n)} \not \in O_j$ et $y_{\phi(n)} \to x$ 