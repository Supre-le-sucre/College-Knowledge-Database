## Théorème de Bolzano-Weierstrass
On énonce le théorème sur la compacité suivant: #!

$$\forall a < b, [a,b] \text{ est un compact}$$
<!--ID: 1729505064091-->



### Preuve
Soit $(x_n)_{n \in \mathbb N}$ une suite dans $[a,b]$ montrons qu'il existe une sous-suite convergente dans $[a,b]$.

On rappelle que si $A \subset \mathbb R$ est un ensemble borné, alors il admet une borne supérieur $M$
$$\forall x \in A, x \leq M$$
$$\forall \epsilon > 0, \exists x  \in A, x \geq M-\epsilon$$

On considère la suite $y_n = \sup_{k \geq n}\set{x_k}$
Elle est décroissante, en effet, si on considère $A_n = \set{x_k, k \geq n}$ alors $A_{n+1} \subseteq A_n$. L'ensemble Et si $x \in A_n, x \leq M$ on a aussi $x \in A_{n+1}, x \leq M$

Or comme $y_n$ est une suite de $[a,b]$, elle est donc minorée, donc elle converge vers un élément $L$. On peut donc établir une limite candidate.

Essayons d'établir une sous-suite de $x_n$ convergente vers $L$
Par hypothèse on sait que

$$\forall \epsilon > 0, \exists N \in \mathbb N, \forall n > N, y_n \in B(L, \epsilon)$$
Et par définition de la borne sup ré énoncée précédemment... 
$$\forall k \geq n, \; x_k \leq y_n$$
$$\forall \epsilon > 0, \exists x_\epsilon, \; y_n-\epsilon \leq x_\epsilon \leq y_n$$

On cherche $\phi$ strictement croissant telle que, à partir d'un certain rang $x_{\phi(n)} \in B(L, \epsilon)$

Pour $\epsilon = 1$ les hypothèses nous donnent que
$$\exists N(1) > 0, y_{N(1)} \in B(L, 1)$$
Et aussi $$\exists N(2) > N(1), x_{N(2)} \in [y_{N(1)}-1, y_{N(1)}]$$ donc $$x_{N(2)} \in B(L, 2)$$

Puis pour $\epsilon = \frac{1}{2}$ les hypothèses nous donnent que
$$\exists N(3) > N(2), y_{N(2)} \in B(L, \frac{1}{2})$$
Et aussi $$\exists N(4) > N(3), x_{N(3)} \in [y_{N(2)}-\frac{1}{2}, y_{N(2)}]$$ donc $$x_{N(2)} \in B(L, 1)$$

Par itération successive, si on pose $\epsilon_k = \frac{1}{2^k}$ On obtient une suite de $(N_n)_{n \in \mathbb N}$ strictement croissante, telle que, à partir d'un certain rang, on a que
$$x_{N(n)} \in B(L, \frac{1}{2^{k-1}})$$
$$\tag*{$\blacksquare$}$$

## Propriété sur la compacité de $\mathbb R^n$ et la fermeture
On observe que: #!

Les sous-espaces compacts de $(\mathbb R^n, ||\cdot||)$ sont les fermés bornés.
<!--ID: 1729505040481-->


### Preuve
$\Rightarrow$ Montrons qu'un espace compact de $(\mathbb R^n, ||\cdot||)$ est un fermé borné.
On a déjà vu précédemment [[Compacité#Propriété sur la compacité d'un espace et sa fermeture|qu'un espace compact est un fermé]]. Il ne reste donc plus qu'à montrer qu'il est borné.

On raisonne par contraposée, montrons donc qu'un espace non borné n'est pas compact.
Trouvons une suite de $A$ n'admettant pas de sous-suite convergente.
Comme $A$ est non borné, il existe $(x_n)$ tel que $||x_{n}|| \to + \infty$
Or toute suite convergente est borné, mais ce n'est pas le cas de $(x_n)$ donc elle ne peut pas admettre de sous-suite bornée.

$\Leftarrow$ Soit $A$ un fermé borné de $\mathbb R^n$, montrons qu'il est compact.

Comme $A$ est borné, on a donc $R$ tel que $A \subset [-R, R]^n$ et $\overline{A} \subset [-R, R]^n$
Comme $\overline{A}$ est un fermé de $\mathbb R^n$, alors on a que $\overline{A} = A$ et $[-R, R]^n$ est un compact d'après Weierstrass.
Est un fermé d'un compact, donc il est compact.


