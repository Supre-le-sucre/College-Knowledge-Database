#algebre 
## Permutation sur polynôme

### Action de $S_n$ sur $\mathbb Z[X]$
Soit $n \in \mathbb{N}^*$, pour $\sigma \in S_n$ dans le [[Groupe symmétrique]] et $f(X_{1}, \cdots X_{n}) \in\mathbb{Z}[X_{1}, \cdots, X_{n}]$, on fait agir $S_n$ sur $\mathbb{Z}[X_{1},\cdots X_n]$ par:
$$\sigma.P=P(X_{\sigma(1)}, \cdots X_{\sigma(n)})$$
### Associativité et distributivité de la permutation
Pour $\sigma, \tau \in S_n$, on aurait alors
$$\sigma.(\tau P) = \sigma.P(X_{\tau(1)}, \cdots, X_{\tau(n)}) = P(X_{\sigma \circ\tau(1)}, \cdots, X_{\sigma \circ\tau(n)}) = \sigma\tau.P$$
On a aussi:
$$\sigma.(P+\lambda Q) = \sigma.P + \lambda\sigma.Q$$
Et de même pour le produit:
$$\sigma.(PQ) = (\sigma.P)(\sigma.Q)$$
### Différente d'un polynôme
On définit la différente d'un polynôme $\mathbb Z[X_{1}, \cdots, X_{n}]$comme étant:
$$\Delta= \prod_{1\leq i < j \leq n}(X_{i}- X_{j})$$
## Définition de la signature d'une permutation

### Théorème
$\forall \sigma \in S_n,$ on a que $\sigma.\Delta = \epsilon(\sigma)\Delta$  (cf.[[#Différente d'un polynôme]]) avec $\epsilon(\sigma) \in \set{\pm1}$.

L'application $\epsilon : (S_{n}, \circ) \to (\mathbb{Z}/2\mathbb{Z}, \times)$ appelée signature est un [[Morphismes de groupes]]

#### Preuve
Considérons la transposition $\tau=(rs)$ avec $1 \leq r < s \leq n$. Calculons $\tau.\Delta$, on a alors:
$$\tau.\Delta = \prod_{1\leq i < j \leq n}(X_{\tau(i)}- X_{\tau(j)})=\prod_{1\leq i < j \leq n}\tau.(X_{i}- X_{j})$$
On a déjà que $\tau.(X_r-X_{s})= -(X_r-X_s)$  
Si un facteur ne contient pas $X_r$ ou $X_s$, il est inchangé.
Pour les autres facteurs, observons...

$$\forall k \not \in \set{r,s},\tau.(X_{k}-X_{s})(X_k-X_{r}) = (X_{k}-X_{r})(X_k-X_{s})$$
Ils restent donc inchangés.

On en déduit alors que $\tau.\Delta = - \Delta$
Ainsi puisque $S_n$ est engendré par des transpositions on alors que $\sigma.\Delta=\pm\Delta$.
On définit alors $\epsilon(\sigma) = \set{\pm1}$ tel que:
$$\sigma.\Delta= \epsilon(\sigma)\Delta$$

Vérifions qu'il s'agit bien d'un [[Morphismes de groupes]]...
On a qu'indubitablement $\epsilon(Id) = 1$
Observons que grâce à [[#Associativité et distributivité de la permutation]], on a que:
$$\epsilon(\sigma\sigma')\Delta = (\sigma\sigma'.\Delta) = \sigma.(\sigma'\Delta) = \sigma.(\epsilon(\sigma')\Delta) = \epsilon(\sigma')\sigma.\Delta = \epsilon(\sigma)\epsilon(\sigma')\Delta$$

$$\tag*{$\blacksquare$}$$

### Corollaire
Pour tout transposition, on a $\epsilon(\tau)=-1$ et pour tout $r$-cycle $\sigma$, on a $\epsilon(\sigma) = (-1)^{r-1}$

#### Preuve
On a déjà prouvé précédemment que $\epsilon(\tau)=-1$ . Enfin, si $\sigma = (a_{1},\cdots, a_k)$ on a que [[Cycle#Toute permutation est un produit de permutation|une permutation est un produit de permutation]] qui peut donc être ramené à un produit de transpositions. Il s'agit donc le produit de $r-1$ transpositions.
$$\tag*{$\blacksquare$}$$

