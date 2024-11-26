#topo
## Définition
Soit $(X, d_X)$ et $(Y, d_Y)$ et $f:(X, d_X) \to (Y, d_Y)$, on dit que $f$ est continue en $x_o \in X$ si et seulement si: #!

$$\forall \epsilon > 0, \exists\eta >0, d_X(x_0, x)< \eta \implies d_Y(f(x_0), f(x)) < \epsilon$$
<!--ID: 1729504947058-->



## Proposition sur les ouverts et la continuité
Soit $f: X \to Y$ avec $(X, d_X)$ et $(Y, d_Y)$ on observe que: #!

$f$ est continue sur $X$ si et seulement si $$\forall O \subseteq Y \text{ un ouvert}, f^{-1}(O) \text{ est aussi un ouvert}$$
<!--ID: 1729504947060-->


### Preuve
$\Rightarrow$: Supposons $f$ continue


Soit $O$ un ouvert de $Y$, montrons que $f^{-1}(O)$ est un ouvert de $X$
Soit $x  \in f^{-1}(O)$, montrons que $\exists \eta > 0$ tel que $B(x, \eta) \subseteq f^{-1}(O)$

On sait par hypothèse que $f(x) \in O$
Comme $O$ est un ouvert, alors $\exists \epsilon > 0,  B(f(x), \epsilon) \subseteq O$
De plus étant donné que $f$ est continue, $\exists \eta > 0$ tel que $y \in B(x, \eta) \implies f(y) \in B(f(x), \epsilon)$

Donc prenons $y \in B(x, \eta)$ et observons donc que $f(y) \in B(f(x), \epsilon) \subseteq O$. Donc finalement, ceci implique bien que $y \in f^{-1}(O)$.

$\Leftarrow$: On aimerait savoir si $f$ est continue. Posons sobrement $x \in X$

Soit $\epsilon > 0$, $B(f(x), \epsilon)$ est un ouvert de $Y$. Donc $f^{-1}(B(f(x), \epsilon))$ est un ouvert de de $X$
De plus $x \in f^{-1}(B(f(x), \epsilon))$ car rappelons que
$$f^{-1}(B(f(x), \epsilon)) = \set{y \in X, f(y) \in B(f(x), \epsilon)}$$

Donc finalement, comme $f^{-1}(B(f(x), \epsilon))$ est un ouvert, on a qu'il existe $\eta > 0$ tel que
$$B(x, \eta) \subseteq f^{-1}(B(f(x), \epsilon))$$
C'est terminé: $y \in B(x, \eta) \implies y \in f^{-1}(B(f(x), \epsilon)) \implies f(y) \in B(f(x), \epsilon)$ 
$$\tag*{$\blacksquare$}$$

## $k$-Lipchitzienne
Pour $X, Y$, 2 espaces métriques, on définit une fonction $f: X \to Y$ $k$-Lipchitzienne comme étant: #!

Pour $k \in \mathbb R^+$...
$$\forall(x, x') \in X^2, d_Y(f(x), f(y)) \leq kd(x,y)$$
**Remarque**: Il s'agit d'un cas particulier de la continuité.
<!--ID: 1729504947063-->



## Caractérisation séquentielle de la continuité
On pose deux espaces métriques $X$ et $Y$ #!

$f: X \to Y$ est continue en $x$, si et seulement si, $\forall (x_n)_{n \in \mathbb N}$ tel que $x_n \to x$ on a $f(x_n) \to f(x)$ 
<!--ID: 1729504947066-->



### Preuve
$\Rightarrow$ On a que $f$ est continue au point $x$ avec $x_n \to x$

$$\forall \epsilon> 0, \exists \eta > 0, y \in B(x, \eta) \implies f(y) \in B(f(x), \epsilon)$$
$$\forall \eta > 0, \exists N \in \mathbb N, \forall n \geq N, x_n \in B(x, \eta)$$
On aimerait donc avoir
$$\forall \epsilon > 0, \exists N \in \mathbb N, \forall n \geq N, f(x_n) \in B(x, \epsilon)$$
Soit $\epsilon > 0$ on pose $x_n \in B(x, \eta)$ et donc on a bien $f(x_n) \in B(f(x), \epsilon)$

$\Leftarrow$: On résonne par contraposée
Sachant que $f$ n'est pas continue, on veut montrer qu'il existe une suite $(x_n)_{n \in \mathbb N}$ telle que $x_n \to x$ mais $f(x_n) \not \to f(x)$ 

On suppose donc...
$$\exists \epsilon>0, \forall \eta > 0, y \in B(x, \eta) \text{ et } f(y) \not\in B(f(x), \epsilon)$$
Posons $\eta = \frac{1}{n}$, alors $\forall n \in \mathbb N^*, \exists x_n \in B(x, \frac{1}{n})$ telle que $f(x_n) \not\in B(f(x), \epsilon)$
C'est terminé
$$\tag*{$\blacksquare$}$$
