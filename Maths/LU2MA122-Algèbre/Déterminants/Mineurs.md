## Définition
Soit $M \in M_n(A)$ et $r \in [1,n]$
On se donne des indices $1 \leq i_1 < \dots < i_r \leq n$ et $1 \leq j_1 < \dots < j_r \leq n$ autrement dit on prends $r$ indices de lignes et $r$ indices de colonnes, tous différents.
On appelle mineurs d'ordre $r$ de $M$ le nombre: #!
$$\det((m_{i_k,j_l})_{1 \leq k \leq r, 1\leq l\leq r})$$ Notons qu'il existe donc $\binom{n}{r}^2$ mineurs différents d'ordre $r$, car il s'agit de choisir deux fois $r$ éléments parmi $n$ ($i$ et $j$)
<!--ID: 1713558248365-->


## Théorème du rang par mineur
On énonce le théorème suivant: #!

Soit $\mathbb K$ un corps, avec $M \in M_n(\mathbb K)$, $r \in [1,n]$, on a que que $rang(M) \geq r$ si et seulement si il existe un mineur d'ordre $r$ non nul.
Il est ==fondamental== de travailler avec un corps. En général il n'y a pas de notion de rang.
<!--ID: 1713558248369-->

### Preuve
Soient $C_1, \dots, C_n$ les colonnes de $M$

