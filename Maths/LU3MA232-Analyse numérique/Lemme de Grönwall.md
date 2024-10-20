## Lemme de Grönwall continue
On observe le phénomène suivant: #!

Soit $y: [0, T] \to \mathbb R$ une fonction dérivable vérifiant
$$\forall t \in [0, T], y'(t) \leq a(t)y(t)+b(t)$$où $a: [0, T] \to \mathbb R$ et $b: [0, T] \to \mathbb R$ deux fonctions continues. En notant $A(t) = \int_0^ta(s)ds$ la primitive de $a$ s'annulant en $0$. Alors pour tout $t \in [0, T]$ on a que
$$y(t) \leq e^{A(t)}y(0) + \int_0^te^{A(t)- A(s)}b(s)ds$$

## Lemme de Grönwall discret
On observe le phénomène suivant: #!

Soit $y_n$ une suite de réels vérifiant
$$y_{n+1} - y_n \leq a y_n+b_n$$avec $a > -1$ Alors on a que: