## Définition
Soit $M \in M_n(A)$, on considère le polynôme caractéristique de $M$ comme étant: #!
$$\mathcal X_M(X) = \det(XI_n-M)$$
<!--ID: 1713558248325-->


## Proposition sur la forme du polynôme caractéristique
Soit $M\in M_n(A)$ alors $\mathcal X_M$ est unitaire de degré $n$ avec en particulier: #!
$$\mathcal X_M(X) = X^n - Tr(M)X^{n-1} + \cdots +(-1)^n\det(A)$$
<!--ID: 1713558248330-->


## Proposition sur les valeurs propres de $M$
Soit $\mathbb K$ un corps et $M \in M_n(\mathbb K)$, alors $\lambda \in \mathbb K$ est une valeur propre de $M$: #!
si et seulement si $\lambda$ est une racine de $\mathcal X_M$. En particulier, $M$ admet donc au plus $n$ valeurs propres.
<!--ID: 1713558248334-->


### Preuve
$\Rightarrow$
Si $\lambda \in \mathbb K$ est une valeur propre, alors il existe $x \in \mathbb K^n$ tel que $Mx = \lambda x$, soit alors:
$$Mx = \lambda x \Leftrightarrow Mx - \lambda x = 0 \Leftrightarrow (MId - \lambda Id)x =0 \Leftrightarrow (M - \lambda Id)x = 0$$
Ainsi donc on que:
$$\det((M-\lambda Id)x)  =0 \Leftrightarrow \det(M-\lambda Id)\det(x) =0$$
Puisque $x$ est un vecteur non nul, son déterminant est non nul. D'où finalement
$$\det(M -\lambda Id) = 0$$
Ceci implique que $\lambda$ est une racine de $\mathcal X_M$

$\Leftarrow$
Soit $\lambda$ une racine de $\mathcal X_M$ tel que, donc, $\det(M -\lambda Id) = 0$
On a alors que la matrice $M- \lambda Id$ n'est pas inversible.
On a donc en particulier que $Ker(M-\lambda Id) \not = \{0\}$, et donc qu'il existe un $x$ tel que
$(M-\lambda Id).x = 0$ autrement dit que $Mx - \lambda x = 0 \Leftrightarrow Mx = \lambda x$
$$\tag*{$\blacksquare$}$$

## Matrices semblables

### Définition de matrices semblables
Deux matrices $A$ et $B$ sont dites semblables, s'il existe une matrice inversible $P$ tel que: #!
$$A = PBP^{-1}$$
<!--ID: 1713558248338-->


### Propriété
Deux matrices semblables ont le même polynôme caractéristique.

#### Preuve
Soit $M$ et $Q$ deux matrices semblables. On a donc $M = PQP^{-1}$
De fait:
$$M - \lambda Id = PQP^{-1} - \lambda Id = PQP^{-1} - \lambda P.Id.P^{-1} = P(Q-\lambda Id)P^{-1}$$
Et d'après la formule du déterminant on a bien
$$\det(M-\lambda Id) = \det(P(Q-\lambda Id)P^{-1}) = \det(P)\det(P)^{-1}\det(Q-\lambda Id) = \det(Q-\lambda Id)$$
$$\tag*{$\blacksquare$}$$

## Théorème de la commutativité du produit
Soit $A$ un [[Anneaux]]. On a, concernant le polynôme caractéristique pour $B,C \in M_n(A)$ que: #!
$$\mathcal X_{BC} = \mathcal X_{CB}$$
<!--ID: 1713558248342-->


## Théorème de Cayley-Hamilton
On énonce le théorème suivant: #!

Soit $M \in M_n(A)$ alors $\mathcal X_M(M) = 0$
<!--ID: 1713558248346-->


### Preuve

#### Remarque importante
La preuve de ce théorème, n'est, contrairement à ce que l'on pourrait le croire, non triviale.
En effet, il est faux de dire que:
$$\det(M-XId)(M) = \det(M-M) =0$$
L'intérêt des [[Anneaux]] se concrétise ici, car la notion d'évaluation dans cette égalité est faussée.

Supposons ici que $A = \mathbb Z$, la matrice $X - XId$ est donc dans $M_n(\mathbb Z[X])$. En évaluant $X$ pour une certaine matrice $K \in M_n(\mathbb Z)$, on considère alors le morphisme d'anneau suivant:
$$\phi_K: \mathbb M_n(Z[X]) \to M_n(M_n(\mathbb Z))$$
Cependant $M_n(\mathbb Z)$ est un anneau non commutatif. En considérant $M_n(M_n(\mathbb Z))$ il n'y aucune théorie du déterminant qui nous permet d'établir un morphisme de monoïdes $M_n(M_n(\mathbb Z)) \to M_n(\mathbb Z)$.

L'évaluation de $M-XId$ en $M$ fait sens, en revanche, l'évaluation selon le déterminant ne l'est pas. L'argument n'est donc aucunement recevable.

#### Début de la vraie preuve
On se propose de considérer l'[[Comatrices#Théorème des produits|identité comatricielle]] du déterminant
$$(XId-M).^tCom(Xid-M) = \mathcal X_M(X)Id$$
On note $\tilde{C} := \:^tCom(Xid-M)$
Comme la matrice des cofacteurs consiste en les [[Mineurs]] d'ordre $n-1$, on écrit:
$$\tilde C = B_0 + B_1 X + \cdots + B_{n-1}X^{n-1} \in M_n(A[X])$$ avec les $B_i \in M_n(A)$. On a donc:
$$(XId-M)(B_0 + B_1 X + \cdots + B_{n-1}X^{n-1}) = a_0Id + \cdots + a_nX^nId = \mathcal X_M(X)Id$$
Il en résulte alors que $MB_0 = -a_0Id, B_0-MB_1 = a_1 Id$ etc.
On multiple alors la première égalité par $Id$, la seconde par $M$ et la dernière par $M^n$
En effectuant la somme de ces 3 égalité on obtient que
$$0 = \mathcal X_M(M)$$
$$\tag*{$\blacksquare$}$$

## Propriété de la matrice inverse
Soit $M \in GL_n(A)$, alors $M^{-1}$ est un polynôme en $M$

### Preuve
Par Cayley-Hamilton on a que:
$$\mathcal X_M(M) = M^n + a_{n-1}M^{n-1} + \cdots + a_0Id = 0$$
On a que par la [[#Proposition sur la forme du polynôme caractéristique]], $a_0 = (-1)^n\det(M)$
De plus comme $M \in GL_n(A)$ on a d'après [[Comatrices#Théorème de l'inverse|ce théorème]] que $\det(M) \in A^\times$, donc $a_0 \in A^\times$.
On peut donc écrire:
$$M.(M^{n-1}+a_{n-1}M_{n-2} + \cdots +a_1Id) = -a_0Id$$
Soit finalement:
$$M^{-1} = -\frac{1}{a_0}(M^{n-1}+a_{n-1}M_{n-2} + \cdots +a_1Id)$$
$$\tag*{$\blacksquare$}$$

## Lien entre la comatrice et le polynôme caractéristique
Soit $\mathbb K$ un corps et $M \in GL_n(\mathbb K)$ posons $Q_M = \frac{(-1)^n\mathcal X_M-\det(M)}{X} \in \mathbb K[X]$ alors on a l'égalité suivante: #!

$$Q_M(M) = \:^tCom(M)$$
<!--ID: 1713558248350-->



## Matrices compagnons

### Définition
Pour un polynôme $P =  X^n + a_{n-1}X^{n-1} + \cdots + a_0 \in A[X]$, on considère la matrice compagnon: #!

La matrice $C$ tel que $\mathcal X_C(X) = P$ soit alors
$$C = \begin{pmatrix}0  &  0  & \cdots  & 0 & -a_0 \\ 1 & 0  & \cdots   & 0 & -a_1 \\ 0 & 1  & \cdots & 0 & -a_2 \\ \vdots & \vdots & \ddots & \vdots & \vdots\\ 0 & 0 & \cdots & 1 & a_{n-1}\end{pmatrix}$$
<!--ID: 1713558248353-->

