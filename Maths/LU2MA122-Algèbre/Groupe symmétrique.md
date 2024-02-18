#algebre
## L'ensemble des bijections est un groupe
### Proposition
Soit un ensemble $E$, on note $\text{Bij}(E)$ l'ensemble des bijections de $E$. Alors $(\text{Bij}(E), \circ)$, où $\circ$ la composition de fonctions, est un [[Groupe]]

### Preuve

On prouve d'abord qu'il s'agit d'un [[Monoïde]]
On a que l'élément neutre est clairement l'application identité $Id_E$
Elle est aussi par définition associative.

Et on prouve ensuite l'existence d'un inverse
Or là encore, cet inverse est trivial.
Soit $\sigma \in \text{Bij}(E)$, alors $\sigma^{-1}$ est clairement son inverse.
$$\tag*{$\blacksquare$}$$

## Définition

$\forall n \in \mathbb{N}^*$ on définit le groupe symétrique $S_n$ tel que:

$S_n = \text{Bij}([1, n])$. Le couple $(S_n, \circ)$, où $\circ$ est la composition de fonction est un groupe. 

## Le cardinal de $S_n$
### Lemme
Pout tout $n \in \mathbb{N}^*$, on a $card(S_n) = n!$ 

### Preuve
Il faut remarquer que l'ensemble des éléments de $S_n$ peuvent être vues comme une simple permutation:
- $\sigma(1)$ peut être associé à $n$ éléments
- $\sigma(2)$ peut être associé à $n-1$ éléments
- ...
-  $\sigma(n)$ ne peut être associé qu'à $1$ élément

Comme il s'agit d'une bijection, on ne compte cette permutation qu'une seule et unique fois.
Par produit on a bien $card(S_n) = n!$ 
$$\tag*{$\blacksquare$}$$

## Engendrement de $S_n$

### Théorème
Le groupe $S_n$ est engendré par les [[Transpositions]]. De plus, il est même engendré par les transpositions $(1i)$ pour $i \in [1,n]$

**Remarque**: La décomposition en produit de transpositions n'est pas commutatif, et il n'existe donc pas d'unicité de la décomposition à permutations de facteurs près.

### Preuve
En se basant sur [[Cycle#Toute permutation est un produit de permutation|ce théorème]], il suffit de montrer qu'un [[Cycle]] est un produit de transposition.

Ceci se remarque immédiatement:
$$(a_{1}, \cdots, a_{k})= (a_{1}a_{2})(a_{2}a_{3})\cdots(a_{k-1}a_k)$$

De plus, on observe $(ij)=(1i)(1j)(1i)$
$$\tag*{$\blacksquare$}$$
