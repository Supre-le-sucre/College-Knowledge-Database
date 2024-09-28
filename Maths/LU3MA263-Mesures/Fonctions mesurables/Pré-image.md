## Définition de la préimage
Soit $E, E'$ 2 ensembles avec $f: E \to E'$ et $B \subseteq E'$, on définit la pré-image de $f$ sur $B$, notée $f^{-1}(B)$ comme étant: #!

$$f^{-1}(B) = \set{x \in E, f(x \in B)} \subseteq E$$
<!--ID: 1727559283088-->


## Propriétés de base
On rappelle les propriétés de base de la pré-image: #!

$$f^{-1}\left(\bigcup_{i \in J} A_i\right) = \bigcup_{i \in J} f^{-1}(A_i)$$
$$f^{-1}\left(\bigcap_{i \in J} A_i\right) = \bigcap_{i \in J} f^{-1}(A_i)$$
$$f^{-1}\left(A_i^c\right) = (f^{-1}(A_i))^c$$
<!--ID: 1727559283090-->


## Continuité topologique de $f$
On considère que: #!

Soit $f : \mathbb R^d \to \mathbb R^d$, on a que $f$ continue si et seulement si $\forall O$ ouvert de $\mathbb R^d$, on a que $f^{-1}(O)$ est un ouvert de $\mathbb R^d$ 
<!--ID: 1727559283091-->
