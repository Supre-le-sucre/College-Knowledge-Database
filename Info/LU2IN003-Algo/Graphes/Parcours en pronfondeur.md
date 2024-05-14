## Définition intuitive
Soit $G = (V, E)$ un graphe non orienté et un sommet $s \in V$. A partir de l'origine $s$ , on visite les sommet le long de la chaîne élémentaire jusqu'à arriver à un sommet sans voisin non visité. On revient alors au dernier sommet sur la chaîne avec un voisin non visité et on recommence.

## Définition
Un parcours en profondeur est un [[Parcours en largeur]] où l'on va visiter le dernier sommet ouvert plutôt que le premier.

On définit un parcours en profondeur mathématiquement de la façon suivante: #!

Soit $G=(V, E)$ un graphe non orienté connexe et $L=(v_1, \dots, v_n)$ un parcours de $G$.
Ce parcours $L$ est dit *"en profondeur"* si pour tout sous-parcours $L_k = (v_1, \dots, v_k)$ le sommet $v_{k+1}$ est un sommet adjacent au ==dernier== sommet [[Parcours#Sommet ouvert et fermé|ouvert]] de $L_k$

## [[Graphes de liaison]] en profondeur

On définit un graphe de liaison en profondeur de la façon suivante: #!

Soit $G = (V, E)$ un [[Graphes non orientés]] qui est [[Graphes non orientés#Connexité|connexe]], et $L = (v_1, \dots, v_n)$ un parcours en profondeur de $G$
On donne le graphe orienté $\mathcal A^*(L) = (V(L), H(L))$ le graphe de liaison en profondeur si:
- $\mathcal A^*(L) = (V(L), H(L))$ est un [[Graphes de liaison]] de $L$
- Pour tout sous-parcours $L_k =(v_1, \dots, v_k)$, $v_{k+1}$ a pour prédécesseur le dernier sommet ouvert de $L_k$
Notons que le graphe de liaison en largeur ==est unique==