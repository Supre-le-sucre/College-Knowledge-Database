## Définition
Soit $A$ un anneau commutatif, on dit que $I \subset A$ est un idéal si #!

$(I, +)$ est un [[Sous-groupe]] et si on a que $$\forall a \in A, a.I = \{ax,x \in I\} \subset I$$

### Remarques
Tirons de la définition d'idéal les remarques suivantes: #!

- Si $I$ est un idéal, et $1 \in I$ alors $I = A$ puisque pour tout $a \in A, a = a.1 \in I$
- En particulier, pour tout $a \in A$, on a que $a.A =\{ax, x \in A\}$ est un idéal de $A$ que l'on note $(a)$ et dit: *"idéal principal"* 
- Plus généralement si $(a_1, \dots, a_r) \in A^r$ on note $(a_1, \dots, a_r)$ l'idéal engendré par ces éléments, il consiste en les combinaisons $\sum_{i=1}^ra_ix_i$ avec les $x_i$ dans $A$

## Idéaux des corps $\mathbb K[X]$
On observe que: #!
Soit $\mathbb K$ un corps, alors tout idéal $\mathbb K[X]$ est principal et admet un unique générateur unitaire

### Preuve
Soit $I\subset \mathbb K[X]$ un idéal non-nul, soit $P \in I$ non-nul de degré minimal $d$, si $d=0$, alors on a que $P$ est une constante inversible et $I =A$. Sinon montrons que $I= (P)$.

Soit $Q \in I$, on effectue la division euclidien de $Q$ par $P$, soit alors $Q = PB +R$ avec $\deg(R) <d$.
Si $R \not = 0$, alors $Q-PB \in I$, donc $R \in I$ et est de degré inférieur à $d$, ce qui contredit la minimalité et $I = (P)$.
Enfin, la preuve donne que tous les générateurs de $I$ sont de mêmes degré, donc différent à une constante près. Ainsi $I$ admet un unique générateur unitaire

## Idéaux des polynômes endomorphique
On observe que: #!

Soient $u \in \mathcal L(E)$ et $x \in E$, alors les ensembles $I_u = \{P \in \mathbb K[X], P(u) = 0\}$ et $I_u(x) = \{P \in \mathbb K[X], P(u)(x) = 0\}$ sont des idéaux de $\mathbb K[X]$, en particulier, ils sont principaux. Soient $\mu_u$ et $\mu_{u,x}$ les générateurs unitaires, on les appelles alors respectivement polynôme minimal, et polynôme minimal ponctuel de $u$. On a $\mu_{u,x}$ divise $\mu_u$ qui divise $\mathcal X_u$

### Preuve
Les ensembles $I_u$ et $I_u(x)$ sont clairement des sous-groupes et pour $P \in I_u$ (resp. $P \in I_u(x)$) et $Q \in \mathbb K[X]$, alors on a que $QP(u) = Q(u)\circ P(u) = 0$ (resp. $QP(u)(x) =  (Q(u) \circ P(u))(x) = 0$)

On a donc que $QP \in I_u$ (resp. $QP \in I_u(x)$). Donc $I_u$ et $I_u(x)$ sont des idéaux, et sont principaux d'après la proposition précédente.
Enfin par [[Polynôme caractéristique#Théorème de Cayley-Hamilton|Cayley-Hamilton]] observons que $\mathcal X_u \in I_u$ donc $\mu_u$ divise $\mathcal X_u$ et comme $\mu_u(u)(x) = 0$ on a aussi que $\mu_{u,x}$ divise $\mu_u$. On sait déjà que les racines de $\mathcal X_u$ sont les valeurs propres de $u$, lme