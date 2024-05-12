## Définition
Soit $A$ un anneau commutatif, on dit que $I \subset A$ est un idéal si #!

$(I, +)$ est un [[Sous-groupe]] et si on a que $$\forall a \in A, a.I = \{ax,x \in I\} \subset I$$

### Remarques
Tirons de la définition d'idéal les remarques suivantes: #!

- Si $I$ est un idéal, et $1 \in I$ alors $I = A$ puisque pour tout $a \in A, a = a.1 \in I$
- En particulier, pour tout $a \in A$, on a que $a.A =\{ax, x \in A\}$ est un idéal de $A$ que l'on note $(a)$ et dit: *"idéal principal"* 
- Plus généralement si $(a_1, \dots, a_r) \in A^r$ on note $(a_1, \dots, a_r)$ l'idéal engendré par ces éléments, il consiste en les combinaisons $\sum_{i=1}^ra_ix_i$ avec les $x_i$ dans $A$

## Idéaux des corps $\mathbb K[X]$
Soit $\mathbb K$ un corps, alors tout idéal $\mathbb K[X]$ est principal et admet un unique générateur unitaire

### Preuve
Soit $I\subset \mathbb K[X]$ un idéal non-nul, soit $P \in I$ non-nul de degré minimal $d$, si $d=0$, alors on a que $P$ est une constante inversible et $I =A$. Sinon montrons que $I= (P)$.

Soit $Q \in I$, on effectue la division euclidien de $Q$ par $P$, soit alors $Q = PB +R$ avec $\deg(R) <d$.
Si $R \not = 0$, alors $Q-PB \in I$, donc $R$