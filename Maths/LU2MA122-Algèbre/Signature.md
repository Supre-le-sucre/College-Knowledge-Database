
## Permutation sur polynôme

### Action de $S_n$ sur $\mathbb Z[X]$
Soit $n \in \mathbb{N}^*$, pour $\sigma \in S_n$ une transposition dans le [[Groupe symmétrique]] et $f(X_{1}, \cdots X_{n}) \in\mathbb{Z}[X_{1}, \cdots, X_{n}]$, on fait agir $S_n$ sur $\mathbb{Z}[X_{1},\cdots X_n]$ par:
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

### Preuve
Considérons la transposition $\tau=(rs)$ avec $1 \leq r < s \leq n$. Calculons $\tau.\Delta$, on a alors:
$$\tau.\Delta = \prod_{1\leq i < j \leq n}(X_{i}- X_{\tau(j)})$$
