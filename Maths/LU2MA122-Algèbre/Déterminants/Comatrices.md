## Définition
Soit $M \in M_n(A)$, on définit la comatrice de $M$ la matrice $Com(M)$ telle que: #!

$$\forall(i,j) \in [1,n]^2, Com(M)_{i,j} = (-1)^{i+j}M_{ij}$$
Où $M_{ij}$ est le déterminant de la matrice $M$ auquel on a retiré la ligne $i$ et la colonne $j$.
On appelle le nombre $(-1)^{i+j}M_{ij}$ le ==cofacteur== de $M$ d'indice $(i,j)$. La comatrice de $M$ est alors, plus sobrement, la matrice de ses cofacteurs.
<!--ID: 1713558248373-->


## Transposition
On peut constater l'égalité suivante: #!
$$Com(^tM) = \:^tCom(M)$$
<!--ID: 1713558248376-->


### Preuve
Cette propriété est triviale si l'on admets le [[Déterminant matriciel#Théorèmes sur le déterminant d'une matrice|2e point sur le théorème du déterminant]]: $det(A) = det(^tA)$. La transposition ne faisant qu'inverser les lignes et les colonnes.

## Théorème du développement du déterminant
On a les égalité suivante qui permettent de simplifier le calcul du déterminant: #!

Considérant $M_{ij}$ est le déterminant de la matrice $M$ auquel on a retiré la ligne $i$ et la colonne $j$.
1. Le développement par rapport à la j-eme colonne est tel que: $$\forall j \in [1,n], det(M) = \sum^n_{i=1}m_{i,j}M_{ij}$$
2. Le développement par rapport à la i-eme ligne est tel que: $$\forall i \in [1,n], det(M) = \sum^n_{j=1}m_{i,j}M_{ij}$$
<!--ID: 1713558248379-->


### Preuve
On considère $(C_1, \dots, C_n)$ les colonnes de la matrice $M=(m_{i,j})$. Et considérons aussi une base canonique $(E_1, \dots, E_n)$ constitué de vecteurs de dimension $n$.

Pour un $k$ fixé, il est normal d'obtenir alors que $C_k = \sum^n_{i=1} m_{ik}E_i$, car $C_k$ est une combinaison linéaire dans la base $(E_1, \dots, E_n)$.
D'après la [[Multi linéarité du déterminant|n-linéarité du déterminant]] on a que:
$$\det(M) = \det(C_1, \dots, C_n) = \sum_{i=1}^nm_{ik}\det(C_1, \dots, C_{k-1}, E_i, C_{k+1}, \dots, C_n)$$

Soit la [[Cycle|permutation]] $\sigma = (1 \cdots k)$ de [[Signature]] $\epsilon(\sigma) = (-1)^{k-1}$. En appliquant $\sigma$ au déterminant, on a alors:
$$\det(C_1, \dots, C_{k-1}, E_i, C_{k+1}, \dots, C_n) = (-1)^{k-1}\det(E_i, C_1, \dots, C_{k-1}, C_{k+1}, \dots, C_n)$$

Observons maintenant les lignes. N'oublions pas l'égalité matricielle suivante:
$$(E_i, C_1, \dots, C_{k-1}, C_{k+1}, \dots, C_n) = 
\begin{pmatrix} 0 & L_1  \\ \vdots & \vdots \\ 1 & L_i \\ \vdots & \vdots \\ 0 & L_n\end{pmatrix}$$ En permutant la i-ème ligne à l'aide $\sigma' = (1 \cdots i)$ (avec $\epsilon(\sigma') = (-1)^{i-1}$) On obtient donc le déterminant:
$$\det\begin{pmatrix} 0 & L_1  \\ \vdots & \vdots \\ 1 & L_i \\ \vdots & \vdots \\ 0 & L_n\end{pmatrix} = (-1)^{i-1}\det\begin{pmatrix} 1 & L_i \\ 0 & L_1  \\ \vdots & \vdots \\ 0 & L_{i-1} \\ 0 & L_{i+1} \\ \vdots & \vdots \\ 0 & L_n\end{pmatrix} = (-1)^{i-1}\det\begin{pmatrix} L_1 \\ \vdots \\ L_{i-1} \\ L_{i+1}  \\ \vdots  \\ L_n\end{pmatrix}$$
En effet, en développant le déterminant par la première ligne, on obtient l'égalité avec le membre tout à droite.

Or rappelons que:
$$\det(C_1, \dots, C_{k-1}, E_i, C_{k+1}, \dots, C_n) = (-1)^{k-1}\det(E_i, C_1, \dots, C_{k-1}, C_{k+1}, \dots, C_n)$$
et que
$$\det (E_i, C_1, \dots, C_{k-1}, C_{k+1}, \dots, C_n) = 
(-1)^{i-1}\det\begin{pmatrix} L_1 \\ \vdots \\ L_{i-1} \\ L_{i+1}  \\ \vdots  \\ L_n\end{pmatrix}$$

Donc on a:
$$\det(C_1, \dots, C_{k-1}, E_i, C_{k+1}, \dots, C_n) = (-1)^{k-1}(-1)^{i-1}\det\begin{pmatrix} L_1 \\ \vdots \\ L_{i-1} \\ L_{i+1}  \\ \vdots  \\ L_n\end{pmatrix}$$

D'où finalement:
$$\det(C_1, \dots, C_n) = \sum_{i=1}^nm_{ik}\det(C_1, \dots, C_{k-1}, E_i, C_{k+1}, \dots, C_n)$$
$$\det(C_1, \dots, C_n) = \sum_{i=1}^nm_{ik}(-1)^{k-1}(-1)^{i-1}\det\begin{pmatrix} L_1 \\ \vdots \\ L_{i-1} \\ L_{i+1}  \\ \vdots  \\ L_n\end{pmatrix}$$
Or on rappelle que la colonne $k$ a été retirée en même temps que la ligne $i$. Donc il s'agit du déterminant de $M$ auquel on a retiré la ligne $i$ et la colonne $k$
$$\det(C_1, \dots, C_n) = \sum_{i=1}^nm_{ik}M_{ik}$$
Etant donné l'égalité du déterminant pas transposition mentionné [[Déterminant matriciel#Théorèmes sur le déterminant d'une matrice|ici]], l'autre point se déduit du premier
$$\tag*{$\blacksquare$}$$

## Théorème des produits
Soit $M \in M_n(A)$ on remarque l'égalité suivante pour $M.^tCom(M)$: #!
$$M.^tCom(M) = \:^tCom(M).M = \det(M)Id$$
<!--ID: 1713558248382-->


## Théorème de l'inverse

### Définition du groupe linéaire
Pour un anneau commutatif $A$ on appelle groupe linéaire sur $A$ l'ensemble: #!
$$GL_n(A) = \{M \in M_n(A), \exists B \in M_n(A), MB=Id\}$$
<!--ID: 1713558248386-->


### Théorème
On a que $GL_n(A) = \{M\in M_n(A), \det(M) \in A^\times\}$. En particulier, on a que pour tout $M \in GL_n(A)$: #!
$$M^{-1} = \frac{1}{\det(M)}\;^tCom(M)$$
L'inverse à droite est aussi l'inverse à gauche, ce qui fait de $GL_n(A)$ un groupe.
<!--ID: 1713558248389-->


### Corollaire
Pour tout $P \in GL_n(A)$ on a d'après le théorème de l'inverse que: #!
$\det(P^{-1}) = \det{(P)}^{-1}$. De plus si $M$ et $Q$ sont semblables dans $M_n(A)$, on a que $\det(M) = \det(Q)$
<!--ID: 1713558248392-->



## Formules de Cramer
On énonce la propriété de la façon suivante: #!

Soit le système linéaire $MX=B$ avec $M \in GL_n(A)$ et $X, B \in A^n$ des vecteurs colonnes. Soit $x_k$ la coordonnée $k$ de $X$. On a que pour tout $k$ dans $[1, n]$: $$x_k = \frac{\det(C_1, \dots, C_{k-1}, B, C_{k+1}, \dots, C_n)}{\det(M)}$$
<!--ID: 1713558248395-->
