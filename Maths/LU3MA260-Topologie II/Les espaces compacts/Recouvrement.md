#topo
## Définition
Soit $(X,d)$. Une famille de partie de $X$ est qualifiée de recouvrement si et seulement si: #!
l'union de ces parties est égale à $X$
<!--ID: 1729505040452-->


## Propriété, recouvrement d'un compact
On observe que l'on peut recouvrir un compact de la façon suivante: #!

$(X, d)$ est un compact, alors
$$\forall \epsilon > 0, \exists(x_1, \dots, x_N), X = \bigcup_{i=1}^NB(x_i, \epsilon)$$
==La réciproque est fausse==: $X=]0,1[$
<!--ID: 1729505040455-->


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

Un espace $(X,d)$ est compact si et seulement si pour tout recouvrement d'ouvert, on peut en extraire un recouvrement fini.
<!--ID: 1729505040457-->


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
On extrait $y_{\phi(n)} \in B(x_{\phi(n)}, \frac{1}{\phi(n)})$ donc $y_{\phi(n)} \not \in O_j$
Observons que $y_{\phi(n)} \to x$, car en effet
$$d(y_{\phi(n)}, x) \leq d(y_{\phi(n)},x_{\phi(n)}) + d(x_{\phi(n)}, x)$$
$$d(y_{\phi(n)}, x) \leq \frac{1}{\phi(n)} + d(x_{\phi(n)}, x)$$
donc $d(y_{\phi(n)}, x) \to 0$
Donc en posant $\epsilon$ comme module de convergence on a que $y_\phi(n) \in B(x, \epsilon) \subset O_j$
Pourtant $y_{\phi(n)} \not \in O_j$. Absurde
$$\tag*{$\blacksquare$}$$

#### Retour à la preuve principale
$\Rightarrow$
Soit $X$ est un compact, et soit $(O_i)_{i \in \Lambda}$ tel que $X = \bigcup_{i \in \Lambda} O_i$
D'après le lemme précédent, alors $$\exists \alpha > 0, \forall x \in X, \exists i \in \Lambda, B(x, \alpha) \subset O_i$$
Et d'après la [[#Propriété, recouvrement d'un compact]], on a alors $$(x_1, \dots, x_n), X = \bigcup_{i = 1}^nB(x_i, \alpha) \subset \bigcup_{i \in \Lambda} O_i = X$$
Donc on a bien extrait un recouvrement d'ouvert fini.

$\Leftarrow$
Par contraposée, $X$ est non compact, donc on veut montrer $\exists (O_i)_{i \in \Lambda}$ ouverts tel que $\bigcup_{i \in \Lambda} O_i = X$, avec $\forall n \in \mathbb N^*, \forall (i_1, \dots, i_N) \in \Lambda^N, \bigcup_{j=1}^NO_{i_j} \subsetneq X$  

Or $X$ non compact, alors $\exists (x_n)_{n \in \mathbb N}$ qui n'admet aucune sous-suite convergente
Donc
$$\forall x \in X, \exists \epsilon_x > 0, \forall N_x > 0, \exists n > N_x, x_n \not \in B(x, \epsilon_x)$$
Et $X = \bigcup_{x \in X} B(x, \epsilon_x)$
S'il existe $(y_1, \dots, y_n) \in X$ tel que $X = \bigcup_{i=1}^N B(y_i, \epsilon_{y_i})$
Alors $\exists i \in [1, n]$ tel que l'ont a une infinité d'élément de la suite $(x_n)_{n \in \mathbb N}$ dans la boule $B(y_i, \epsilon_{y_i})$
Ceci est absurde car par construction, il ne devrait y avoir qu'un nombre fini d'élément.
$$\tag*{$\blacksquare$}$$


