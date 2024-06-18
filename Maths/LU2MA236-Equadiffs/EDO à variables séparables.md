# Définition
On dit qu'une EDO est "à variable séparables" si et seulement si: #!

L'équation peut s'écrire sous la forme $x' g(x) = h(t)$ où $g$ et $h$ sont des fonctions quelconques

# Méthode
Une EDO à variable séparable peut être résolue simplement sous certaines conditions

En rappelant qu'une telle équation est de la forme $x' g(x) = h(t)$
- Il faut trouver une primitive de $g$ et de $h$, que l'on nomme respectivement $G, H$ et appliquer la formule de dérivation interne pour obtenir une nouvelle égalité: $$G(x) = H(t) + c \;| \; c \in \mathbb R$$
- A partir de là, il faut trouver une formule pour la bijection réciproque de $G$, ntons $G^{-1}$. La solution de l'équation est alors: $$x(t) = G^{-1}(H(t) + c)$$