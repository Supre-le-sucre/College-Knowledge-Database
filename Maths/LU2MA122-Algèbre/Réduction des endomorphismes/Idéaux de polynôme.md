## Définition
Soit $A$ un anneau commutatif, on dit que $I \subset A$ est un idéal si #!

$(I, +)$ est un [[Sous-groupe]] et si on a que $$\forall a \in A, a.I = \{ax,x \in I\} \subset I$$
<!--ID: 1715537862433-->


### Remarques
Tirons de la définition d'idéal les remarques suivantes: #!

- Si $I$ est un idéal, et $1 \in I$ alors $I = A$ puisque pour tout $a \in A, a = a.1 \in I$
- En particulier, pour tout $a \in A$, on a que $a.A =\{ax, x \in A\}$ est un idéal de $A$ que l'on note $(a)$ et dit: *"idéal principal"* 
- Plus généralement si $(a_1, \dots, a_r) \in A^r$ on note $(a_1, \dots, a_r)$ l'idéal engendré par ces éléments, il consiste en les combinaisons $\sum_{i=1}^ra_ix_i$ avec les $x_i$ dans $A$
<!--ID: 1715537862435-->


## Idéaux des corps $\mathbb K[X]$
On observe que: #!
Soit $\mathbb K$ un corps, alors tout idéal $\mathbb K[X]$ est principal et admet un unique générateur unitaire
<!--ID: 1715537862436-->


### Preuve
Soit $I\subset \mathbb K[X]$ un idéal non-nul, soit $P \in I$ non-nul de degré minimal $d$, si $d=0$, alors on a que $P$ est une constante inversible et $I =A$. Sinon montrons que $I= (P)$.

Soit $Q \in I$, on effectue la division euclidien de $Q$ par $P$, soit alors $Q = PB +R$ avec $\deg(R) <d$.
Si $R \not = 0$, alors $Q-PB \in I$, donc $R \in I$ et est de degré inférieur à $d$, ce qui contredit la minimalité et $I = (P)$.
Enfin, la preuve donne que tous les générateurs de $I$ sont de mêmes degré, donc différent à une constante près. Ainsi $I$ admet un unique générateur unitaire

## Idéaux des polynômes endomorphique
On observe que: #!

Soient $u \in \mathcal L(E)$ et $x \in E$, alors les ensembles $I_u = \{P \in \mathbb K[X], P(u) = 0\}$ et $I_u(x) = \{P \in \mathbb K[X], P(u)(x) = 0\}$ sont des idéaux de $\mathbb K[X]$, en particulier, ils sont principaux. Soient $\mu_u$ et $\mu_{u,x}$ les générateurs unitaires, on les appelles alors respectivement polynôme minimal, et polynôme minimal ponctuel de $u$. On a $\mu_{u,x}$ divise $\mu_u$ qui divise $\mathcal X_u$
<!--ID: 1715537862438-->


### Preuve
Les ensembles $I_u$ et $I_u(x)$ sont clairement des sous-groupes et pour $P \in I_u$ (resp. $P \in I_u(x)$) et $Q \in \mathbb K[X]$, alors on a que $QP(u) = Q(u)\circ P(u) = 0$ (resp. $QP(u)(x) =  (Q(u) \circ P(u))(x) = 0$)

On a donc que $QP \in I_u$ (resp. $QP \in I_u(x)$). Donc $I_u$ et $I_u(x)$ sont des idéaux, et sont principaux d'après la proposition précédente.
Enfin par [[Polynôme caractéristique#Théorème de Cayley-Hamilton|Cayley-Hamilton]] observons que $\mathcal X_u \in I_u$ donc $\mu_u$ divise $\mathcal X_u$ et comme $\mu_u(u)(x) = 0$ on a aussi que $\mu_{u,x}$ divise $\mu_u$. On sait déjà que les racines de $\mathcal X_u$ sont les valeurs propres de $u$, le [[Valeurs propres et vecteurs propres#Lemme|lemme]] nous dit exactement que ce sont les racines de $\mu_u$

## Relation entre le degré de générateur unitaire et le rang
On observe le lemme suivant: #!

Soit $M \in M_n(\mathbb K)$ alors on a que $\deg(\mu_M) = rg((A^k)_{k \in \mathbb N})$
<!--ID: 1715537862440-->


### Preuve
La minimalité du polynôme minimale implique que son degré est précisément le plus petit entier $r \in \mathbb N$ tel que $(I_n, A, \dots, A^r)$ est liée, ainsi$(I_n, A, \dots, A^{r-1})$ est libre et on a que $r = rg((A^k)_{k \in \mathbb N})$


# Application du polynôme minimal ponctuel

## Théorème
Soient $E$ un $\mathbb K$-espace vectoriel de dimension fini avec $u \in \mathcal L(E)$, alors il existe $x \in E$ tel que $\mu_{u, x} = \mu_u$. Pour un tel $x$ on a donc que $\dim(Vect((u^k(x))_{k \in \mathbb N})) = \deg(\mu_u)$

### Preuve
On écrit $\mu_u = P_1^{r_1} \cdots P_d^{r_d}$ avec les $P_i$ irréductibles. Par le [[Polynômes d'endomorphismes#Lemme des noyaux|lemme des noyaux]] on a donc une décomposition en sous-espaces stables:
$$E = \bigoplus_{i=1}^d \ker P_i^{r_i}(u)$$
Notons $u_i$ la restriction de $u$ à chaque $E_i = \ker P_i^{r_i}(u)$. 
Par définition de $E_i$, on a que $\mu_{u_i}$ qui divise $P_i^{r_i}$.

Si par l'absurde on suppose que $\mu_{u_i} = P_i^\alpha$ avec $\alpha < r_i$, alors en prenant $Q = P_i^\alpha\prod_{j\not = i}P_j^{r_j}$, on annulerait $u$ sur $E$, ce qui contredit la minimalité de $\mu_u$.
Ainsi on a bien $\mu_{u_i} = P_i^\alpha$ 

Et de même si pour tout $x \in K_i, \mu_{u_i, x}$ divise strictement $P_i^{r_i}$ alors on aurait que $P_i^{r_{i-1}}$ annule $u_i$, ce qui contredit la minimalité.
Donc il existe $x_i \in K_i$ tel que $\mu_{u_i, x_i} = \mu_{u, x_i} = P_i^{r_i}$

On pose alors $x = \sum_{i=1}^dx_i$ on a déjà que $\mu_{u,x}$ divise $\mu_u$, montrons donc la réciproque.
Par définition on a que $\mu_{u,x}(u)(x) = 0 = \sum_{i=1}^d\mu_{u,x}(u)(x_i)$. Comme chaque $E_i$ est [[Espaces stables et codiagonalisation|stable]] et comme la somme de des $E_i$ est directe, on obtient donc que
$$\forall 1 \leq i \leq d, \mu_{u,x}(u)(x_i) = 0$$
Ainsi pour tout $î$, $\mu_{u,x} = P_i^{r_i}$ qui divise $\mu_{u,x}$. Et comme ces polynômes sont premiers entre eux, on trouve que $\mu_u$ divise $\mu_{u,x}$ comme souhaité
$$\tag*{$\blacksquare$}$$