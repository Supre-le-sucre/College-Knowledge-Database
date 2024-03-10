#algebre 

## Définition
Pour $M = (m_{ij}) \in M_n(A)$ on définit le déterminant de cet matrice comme: #!
$$det(M) = \sum_{\sigma \in S_n}\epsilon(\sigma)\prod_{i=1}^nm_{\sigma(i)i}$$
<!--ID: 1710069542118-->
**Remarque**: C'est exactement ce que l'on retrouve dans [[Formes n-linéaires alternées#Proposition|la proposition de det(u)]]

### Exemple
On peut observer dans le cas $n=2$ que pour
$$M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$$
On a par définition, que son déterminant est donné par $det(M) = ad-bc$
comme on pourrait effectivement s'y attendre.


## Théorèmes sur le déterminant d'une matrice
Pour $M \in M_n(A)$ on a les propriétés suivantes: #!
1. $det(M) = \prod_{i=1}^nm{ii}$ pour $M$ une matrice triangulaire supérieur
2. $det(M) = det(^tM)$ d'où l'égalité (1) dans le cas triangulaire inférieur également
3. $\forall M, M' \in M_n(A), det(MM')=det(M)det(M')$
<!--ID: 1710069515037-->

### Preuve

On commence d'abord par montrer (1)
Si $M$ est triangulaire supérieure, alors vérifions que pour tout $\sigma \not = Id$ on a qu'il existe $i$ tel que $m_{\sigma(i)i} = 0$, autrement dit, que $\sigma(i) > i$

En effet, résolvons ça par récurrence:
$\Pi(n):$ "Pour tout cycle $\sigma \not = Id$ de $S_n$, $\exists i, \sigma(i) > i$"

B: Pour $n=2$, On a seulement le cycle $\sigma = (1 \quad 2)$ et pour $i=1$, $\sigma(1) = 2 > 1$

H: Montrons $\Pi(n-1) \Rightarrow \Pi(n)$
L'ensemble des cycles $\psi$ de $S_{n-1}$ sont contenus, par [[Cycle#Morphisme canonique|extension]], dans $S_n$
Ainsi l'ensemble des $k$-cycles de $S_n$ $(k \leq n-1)$ ont un $i$ tel que $\sigma(i) > i$ par H.R
Etudions alors les $n$-cycle. On sait qu'un cycle est un [[Cycle#Toute permutation est un produit de permutation|produit de transposition]]. Il suffit alors d'étudier les nouvelles transpositions de $S_n$ (celle de $S_{n-1}$ ayant déjà été évaluée par H.R)

Or ces transpositions étant $(1 \quad n) \dots (n-1 \quad n)$ pour chacune d'entre elle, nous avons bien $i < n$ tel que $\sigma(i) = n > i$

Par récurrence, on alors montré que seul $\sigma = Id$ ne subsiste dans les produit du calcul du déterminant, d'où
$$det(M) = \prod_{i=1}^nm_{ii}$$
$$\tag*{$\blacksquare$}$$
Montrons maintenant (2)
On peut poser part définition l'égalité suivante:
$$det(^tM) = \sum_{\sigma \in S_n}\epsilon(\sigma)\prod_{i=1}^n(^tM)_{\sigma(i)i} = \sum_{\sigma \in S_n}\epsilon(\sigma)\prod_{i=1}^nm_{i\sigma(i)}$$
Pour $\sigma \in S_n$ fixé, on pose $j=\sigma(i)$, pour ainsi obtenir l'égalité suivante:
$$\prod_i^nm_{i\sigma(i)} = \prod_j^nm_{\sigma^{-1}(j)j}$$
Or l'application $\Phi : \sigma \mapsto \sigma^{-1}$ est une bijection de $S_n$ et $\epsilon(\sigma) = \epsilon(\sigma^{-1})$ car $\epsilon$ est un [[Morphismes de groupes]]

D'où finalement...
$$det(^tM) = \sum_{\sigma \in S_n}\epsilon(\sigma^{-1})\prod_{j=1}^nm_{\sigma^{-1}(j)j} = \sum_{\sigma \in S_n}\epsilon(\sigma)\prod_{i=1}^nm_{\sigma(i)i} = det(M)$$
$$\tag*{$\blacksquare$}$$

Enfin montrons (3)
Si on $A = \mathbb K$ est un corps, on l'a alors déjà démontré, car on aura $det(u_M) = det(M)$ si $u_M$ l'endomorphisme associé à la matrice $M$ (cf. [[Formes n-linéaires alternées#Propriété du déterminant sur la composition|propriété du déterminant sur la composition]])

Dans le cas général, l'idéal est de calculer cette égalité comme une égalité polynomiale.
Pour ce faire, considérons l'[[Anneaux]] universel: $\mathbb Z[B_{ij}, C_{ij}]_{1 \leq i,j \leq n}$ avec les matrices universelles $B$ et $C$

