
## Problématique
Soit $E$ un $\mathbb K$-[[Espaces vectoriels]] de dimension finie et $E^\vee$ son dual. Bien que $dim(E^\vee) = dim(E)$, ce deux espaces vectoriels ne sont pas canoniquement isomorphes et il n'existe pas d'application canoniquement vraie entre $E$ et $E^\vee$

## Accouplement canonique entre $E$ et son dual
On définit l'accouplement canonique de $E$ et son dual $E^\vee$ comme étant: #!
$$\forall x \in E, \forall f\in E^\vee, \langle x , f\rangle = f(x)$$
<!--ID: 1709993834147-->


## Flèche canonique entre les endomorphismes de E et de son dual
On peut poser la flèche canonique $\Phi: End(E) \to End(E^\vee)$ donnée par #!
$$\Phi: E^\vee \to E^\vee$$
$$\Phi: u \mapsto\,^tu$$
Où $^tu(f) = f \circ u$  l'adjointe de $u$.
Par construction a l'égalité suivante:
$$\forall x \in E, \forall f \in E^\vee, \langle u(x), f\rangle = \langle x,\, ^tu(f)\rangle$$
<!--ID: 1709993834151-->

### Proposition
La flèche canonique $\Phi$ est un isomorphisme

#### Preuve
Puisque $dim(E) = dim(E^\vee)$ il suffit de prouver l'injectivité.

Soit $u \in End(E)$, tel que $^tu=0_{E^\vee}$. 
On pose les bases $B = (e_1, \dots, e_n)$ de $E$ et $B^* = (e^*_1, \dots e^*_n)$ de $E^\vee$

Comme $u$ est une application linéaire de $E$, il est possible de l'écrire sous forme de matrice.
On pose $u_{i,j}$ les coefficients de sa matrice.

L'objectif étant de montrer que $Ker(\Phi) = \set{0_{E^\vee}}$
Si on montre que $\Phi^{-1}(\set{^tu}) = \set{0_{E^\vee}}$, soit que $u = 0_{E^\vee}$ on aura démontré l'injectivité

Autrement dit, l'objectif final sera de montrer $\forall i, j \; u_{i,j} = 0$

Par hypothèse on a que:
$\forall i \in [1, n], 0_E =$ $^tu(e_i^*) = e_i^*(u) = 0_E$ 
On a alors que l'application $e^*_i u = 0_{E^\vee}$ $\forall i$

Or on a que $e^*_i u (e_j) =u_{i,j}$ car en effet
$$e^*_i=\begin{pmatrix}0 & \cdots & 1 & \cdots & 0\end{pmatrix} \text{ où 1 est à la colonne i et } e_j=\begin{pmatrix}0 \\ \vdots \\ 1 \\ \vdots \\ 0\end{pmatrix} \text { où 1 est à la ligne j} $$
d'où $e^*_i u (e_j) =u_{i,j}$ par produit matriciel

Mais comme $e^*_i u = 0_{E^\vee}$, on a que $e^*_i u (e_j) =u_{i,j} = 0$
Ceci montrant bien l'injectivité

$$\tag*{$\blacksquare$}$$



