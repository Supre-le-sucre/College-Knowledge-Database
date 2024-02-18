## Définition
Pour $1 \leq k \leq n$, on appelle la permutation $\sigma \in S_n$ la  un $k$-cycle caractérisé par le support de cycle $\set{a_1, \cdots, a_k}$  si cette permutation est définie telle que:

$$\forall i, 1 \leq i \leq k-1, \sigma(a_i) = a_{i+1}, \sigma(a_k) = a_1$$
Et l'identité autrement: 
$$ \forall y \not \in \set{a_1, \cdots, a_k}, \sigma(y) = y$$
Si $k=2$ alors on parle de transposition.
On note cette permutation $\sigma = (a_1, \cdots, a_k)$ et que l'on a $\sigma^k = 1$

## Commutativité des cycles à supports disjoints

### Lemme
Soient $\sigma, \sigma' \in S_n$ des cycles à supports disjoints, alors ils commutent

### Preuve
Soient $\sigma=(a_1, \cdots, a_k)$ et $\sigma' = (b_1, \cdots, b_r)$ avec $\set{a_1, \cdots a_k} \cap \set{b_1, \cdots, b_r} = \emptyset$ 

Vérifions s'ils commutent $\forall x$

- Si $x \not \in \set{a_1, \cdots, a_k} \cup \set{b_1, \cdots b_r}$ on a que $\sigma(x) = \sigma'(x) = x$ donc il commutent
- Si $x \in \set{a_1, \cdots, a_k}$ on a que $\sigma'(x) =x$
	Et $\sigma(x) \in \set{a_1, \cdots, a_k}$ donc $\sigma'(\sigma(x)) = \sigma(x)$ et $\sigma(\sigma'(x)) = \sigma(x)$, donc ils commutent
- Si $x \in \set{b_1, \cdots, b_r}$ on a applique la même logique que ci-dessus

Ainsi donc $\sigma$ et $\sigma'$ commutent $\forall x$
$$\tag*{$\blacksquare$}$$
## Morphisme canonique
### Lemme
Soit un sous ensemble $F \subset [1,n]$, il existe un [[Morphismes de groupes]] canonique injectif de la forme:
$$\Phi : (\text{Bij}(F), \circ) \to (S_{n},\circ)$$

De plus observons que si $p = card(F)$, alors on a $\text{Bij}(F) \simeq S_p$.

### Preuve
Pour $\sigma \in \text{Bij}(F)$, il suffit de poser $\Phi(\sigma)$ tel que $\Phi(\sigma)_{|F} = \sigma$ (dit $\Phi$ restreint à $F$, i.e $\forall \sigma \in F, \Phi(\sigma)=\sigma$) et $\Phi(\sigma)_{|F^c} = Id_{|F}$
On a alors que $\Phi(\sigma) \in S_n$ car ils se complètent tout deux pour former une bijection sur $[1,n]$
Et de plus $\Phi$ est injective, car il est différent pour tout $\sigma$ différent

De plus on a que:
$$\Phi(\sigma)_{|F} \circ \Phi(\sigma')_{|F} = \sigma \circ \sigma' = \Phi(\sigma \circ \sigma')_{|F}$$
Et de même dans l'autre restriction.
$$\tag*{$\blacksquare$}$$
## Toute permutation est un produit de permutation
### Théorème
Toute permutation $\sigma \in S_n$ est un produit $\sigma = \sigma_{1}\circ \cdots \circ\sigma_{r}$ de cycles à supports disjoints. Si chaque $\sigma_i$ est de longueur $k_i$ on parle de $k_1 \times \cdots \times k_r$-cycle.

### Preuve
On se propose ici de raisonner par récurrence forte.
Soit $\Pi(n): \sigma \in S_{n}$ admet une décomposition $\sigma = \sigma_{1}\circ \cdots \circ \sigma_{r}$ de cycle à support disjoints

Pour $n=1$, on aura $\sigma \in S_1$, dans ce cas $\sigma = \sigma$ comme produit de cycle à support disjoint

Montrons que $\forall k < n, \Pi(k) \Rightarrow \Pi(n)$
Soit $\sigma \in S_n$.

Si $\sigma(1) = 1$ alors comme $\sigma$ est une bijection, on a que $\sigma([2,n]) = [2,n]$.
On a alors pour $\sigma_{1}= \sigma_{|[2,n]}$ qui induit une permutation de $\text{Bij}([2,n]) \simeq S_{n-1}$.

Par hypothèse de récurrence on aurait donc que $\sigma_1$ est décomposable... 
De plus $\sigma_1$ est une permutation de $S_n$ par prolongement proposé dans [[#Morphisme canonique]]
Ainsi donc $\sigma=\sigma_1$ donc $\sigma$ est bien décomposé en cycles à support disjoints.

Si $\sigma(1) \not = 1$, d'après [[Morphismes de groupes#Lemme sur l'existence d'une puissance neutre autre que 0|ce lemme]] on a qu'il existe $l \in \mathbb{N}^*$ tel que $\sigma^{l}= Id$.
On prend $i_1$ le plus petit entier tel que $\sigma^{i_{1}}(1)= 1$.

On pose alors $\sigma_{1}= (1, \sigma(1), \cdots, \sigma^{i_1-1}(1))$. On note $F_1$ le support de $\sigma_1$.
On a alors l'union disjointe suivante:
$$[1,n] = F_{1}\cup F_1^c$$
Et $\sigma$ est stable sur $F_1$ et son complémentaire:
Si $x \not \in F_1$ et que $\sigma(x) \in F_1$, on a qu'il existe $r \in \mathbb{N}$ tel que $\sigma^{r}(1)= \sigma(x)$, d'où $\sigma^{r-1}(1)= x$ d'où $x \in F_1$ ceci est absurde.

Comme $\sigma$ est injective, on obtient $\sigma' = \sigma_{|F_{1}^{c}}$ une bjection sur $F_1^c$. Par hypothèse de récurrence on alors que $\sigma'$ décomposable et on a que $\sigma = \sigma_{1}\circ \sigma'$, avec $\sigma'$ un élément de $S_n$ par prolongement proposé dans [[#Morphisme canonique]].
$$\tag*{$\blacksquare$}$$

### Proposition
Cette décomposition est unique à permutations de facteurs près.

### Preuve
On pose $\sigma$ en 2 décomposition:
$\sigma=\sigma_{1} \circ \cdots \circ \sigma_r$
$\sigma=\sigma'_{1} \circ \cdots \circ \sigma'_s$
Soit $i \in \text{supp}(\sigma_1)$, alors $\sigma_{1(i)}\not = i$ et il existe $t$ tel que $i \in \text{supp}(\sigma'_t))$.

Or comme les deux sont des cycles, on a $\text{supp}(\sigma_{1})=\set{\sigma^{k(i),}k \in \mathbb{Z}} = \text{supp}(\sigma'_t)$ et $\sigma_1$ = $\sigma'_t$ que l'on peut donc simplifier des deux côté en itérant.
On trouve alors que $r=s$ et $\sigma_{i}= \sigma'_i$ par simple réordonnancement. D'où l'unicité.
$$\tag*{$\blacksquare$}$$