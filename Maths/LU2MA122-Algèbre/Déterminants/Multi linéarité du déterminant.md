## Théorème
Soit $\phi_C : \mathbb K^n \times \dots \times \mathbb K^n \to \mathbb K$ l'application sur les colonnes d'une matrice $M_n$ déterminée par
$(C_1, \dots, C_n) \mapsto det(C_1, \dots, C_n)$. Et soit aussi pour la base canonique de $\mathbb K^n$, la forme $f_{can} \in \Lambda^n\mathbb K^n$ définie par $f(e_1, \dots, e_n) = 1$ #!

On a alors $\phi_C = f_{can}$. Plus particulièrement, $\phi_C$ est une forme $n$-linéaire alternée
Si on pose $\phi_L$ pour les lignes de $M_n$ cette fois, on aura alors $\phi_L = f_{can} \circ tr$ où $tr$ l'application de transposition.
<!--ID: 1710074811655-->


### Preuve
Soit $(C_1, \dots, C_n)$ un $n$-uplet de colonnes, $M$ la matrice associée d'endomorphisme $u_M$.
On a alors par [[Formes n-linéaires alternées#Définition du déterminant|définition]] que
$$f_{can}(C_1, \dots, C_n) = f_{can} \circ u_m(e_1, \dots,e_n) = det(u_m)f_{can}(e_1, \dots, e_n)$$
Or $det(u_m) = det(M)$ comme vu en [[Déterminant matriciel]] d'où...
$$det(u_m)f_{can}(e_1, \dots, e_n) = det(M)f_{can}(e_1, \dots, e_n)= det(M)$$
Or par définition on a:
$$f_can(C_1, \dots, C_n) = det(M) = \phi_C(C_1, \dots, C_n)$$
Pour la remarque sur $\phi_L$, il suffit d'utiliser l'égalité $det(M) = det(^tM)$ (vu [[Déterminant matriciel#Théorèmes sur le déterminant d'une matrice|ici]])
$$\tag*{$\blacksquare$}$$
**Remarque**: Dans le cas d'un [[Anneaux]] commutatif, on dispose de la même manière la forme $f_{can}$ mais elle sera ici $n$-$A$-linéaire et alternée. Ici $n$-$A$ linéaire veut dire que la forme est $A$-linéaire en chacune de ses variables. On dit qu'une application $u : A^n \to A^m$ est $A$-linéaire si
$$u(x+\lambda y) = u(x)+\lambda u(y)$$
avec $\lambda \in A$ et $(x,y) \in A^n$
Il faut noter que cette [[Formes n-linéaires alternées#Proposition|proposition]] s'étend donc aussi dans les anneaux commutatif

### Corollaire
Soit un anneau commutatif $A$, une opérations sur les colonnes du type $$C_i \leftarrow C_i + \sum_{j\not=i}\lambda_jC_j$$ #!
 Ne change pas le déterminant
#### Preuve
Cela vient du fait direct de la linéarité de $\phi_C$ et sa forme alternée
<!--ID: 1710074811664-->

## Propriétés équivalentes
Soit un corps $\mathbb K$ un corps, $m \in M_n(\mathbb K)$ les assertions suivantes sont équivalentes: #!

1. Il existe $X \in \mathbb K^n$ tel que $MX =0$
2. Les colonnes $C_1, \dots, C_n$ de $M$ sont liées
3. On a $det(M) = 0$

## Preuve

Montrons $(1) \Leftrightarrow (2)$ 
Si les colonnes $(C_1, \dots, C_n)$ de $M$ sont liées, alors on a que:
$$\exists(\lambda_1, \dots, \lambda_n) \in \mathbb K^n-\set{0}, \sum^n_{i=1}\lambda_iC_i = 0$$
En posant $X = (\lambda_1, \dots, \lambda_n)$, On aura $MX = 0$
Vice versa, l'existence d'un tel $X$ nous dira que les colonnes sont liées, d'où:
$$\exists(\lambda_1, \dots, \lambda_n) \in \mathbb K^n-\set{0}, \sum^n_{i=1}\lambda_iC_i = 0 \Leftrightarrow MX= 0$$

Montrons $(1) \Leftrightarrow (3)$
D'après le [[Formes n-linéaires alternées#Corollaire|corollaire]] ci-joint, on a $det(M) \not = 0$ si et seulement si $M$ est bijective (car elle admet un inverse dans ce cas). Ainsi donc, si $det(M) = 0$, $M$ n'est pas une bijection, et un tel $X$ non nul existe.
Vice versa, si un tel $X$ non nul existe, alors $M$ n'est pas injective, et ne peut être une bijection.

## Déterminant de Van der Monde
On pose le résultat suivant:
$$V(x_1, \dots, x_n) = \begin{vmatrix}1 & 1 & \cdots & 1  \\ x_1 & x_2 & \cdots & x_n \\ x_1^2 & x_2^2 & \cdots & x_n^2 \\ \vdots & \vdots & \ddots & \vdots \\ x_1^n & x_2^n & \cdots &x_n^n\end{vmatrix} = \prod_{1 \leq i,j \leq n}(x_j-x_i)$$

### Preuve
On effectue pour toutes les lignes l'opérations $L_i \leftarrow L_i - x_1L_{i-1}$ pour $i \geq 2$qui ne [[#Corollaire|ne change pas le déterminant]]
$$V(x_1, \dots, x_n) = \begin{vmatrix}1 & 1 & \cdots & 1  \\ 0 & x_2 -x_1 & \cdots & x_n-x_1\\ 0 & x_2^2-x_1^2x_2 & \cdots & x_n^2 \\ \end{vmatrix}$$ 