## Définition
Soit $(X,d)$ un espace métrique.
On considère $x \in X$ et $V \subseteq X$. On dit que $V$ est un voisinage de $x$ si et seulement si: #!
$$\exists \epsilon > 0, B(x, \epsilon) \subseteq V$$
<!--ID: 1729504946994-->



## Propriété sur la continuité et le voisinage d'une fonction
$f$ est une fonction continue en un point $x \in X$ si et seulement si: #!

L'image réciproque de tout voisinage de $f(x)$ est un voisinage de $x$. Autrement dit: $$\forall V \text{ voisinage de } f(x), \exists \epsilon > 0, B(x, \epsilon) \subseteq f^{-1}(V)$$
<!--ID: 1729504946996-->



### Preuve
$\Rightarrow$: On pose que $f$ est continue en $x$, donc
$$\forall \epsilon > 0, \exists \eta > 0, y \in B(x, \eta) \implies f(y) \in B(f(x), \epsilon)$$

Soit $V$ un voisinage de $f(x)$, donc $\exists \epsilon' > 0, B(f(x), \epsilon') \subseteq V$ 
En appliquant la [[Pré-image]] sur l'inclusion on a que $f^{-1}(B(f(x), \epsilon')) \subseteq f^{-1}(V)$

Comme $f$ est [[Applications continues|continue]] en $x$, on peut poser:
$$\exists \eta > 0, B(x, \eta) \subseteq f^{-1}(B(f(x), \epsilon')) \subseteq f^{-1}(V)$$
(Pour s'en convaincre, regarder le résultat finale de cette [[Applications continues#Preuve|preuve]])
Donc on a bien que $f^{-1}(V)$ est un voisinage de $x$

$\Leftarrow$: Posons ce que l'on sait
$$\forall V \text{ voisinage de } f(x), \exists \tilde V \text{ voisinage de } x, f^{-1}(V) = \tilde V$$
On aimerait résoudre que:
$$\forall \epsilon > 0, \exists \eta > 0, y \in B(x, \eta) \implies f(y) \in B(f(x), \epsilon)$$

Donc posons $\epsilon > 0$
On a que $B(f(x), \epsilon)$ est un voisinage de $f(x)$
Donc en particulier $f^{-1}(B(f(x), \epsilon))$ est un voisinage de $x$ 
On a alors que $\exists \eta > 0$ tel que $B(x \eta) \subseteq f^{-1}(B(f(x), \epsilon))$

Finalement on a que
$$y \in B(x, \eta) \implies f(y) \in B(f(x), \epsilon$$
$$\tag*{$\blacksquare$}$$

## Composition de fonctions et maintiens de la continuité
On considère les 3 espaces métriques $X, Y, Z$...: #!

Pour $f: X \to Y$ et $g: Y \to Z$, 2 applications continues, on a alors que $f \circ g : X \to Z$ est également une application continue.
 
<!--ID: 1729504946999-->

