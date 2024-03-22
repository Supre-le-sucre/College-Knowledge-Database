## Définition
Un graphe est un ensemble de sommets $V$ (pour vertex) et d'arrêtes $E$ (pour edge) qui est une paire de sommet.

## Voisins
On appelle les voisins d'une arrête $v$, l'ensemble de sommets notés $\Gamma(v)$ définie tel que:
$$\Gamma(v) = \set{v' \; | \; \set{v', v} \in E}$$
## Sous graphes
Un sous graphe $SG$ d'un graphe $G$ est un graphe qui contient les certains mêmes sommets et arrêtes que le graphe $G$ sans en ajouter d'avantage.

Un sous graphe $SG$ induit par un ensemble de sommets $V_i$ et un  graphe $G$ est le graphe tel que l'ensemble des arrêtes données dans $SG$ sont connectées entre elles de la même façon qu'elle le sont dans $G$, sans omettre une seule arrête de $G$ entre eux 

## Chaîne
Une chaîne est une séquence de sommets et d'arrêtes tels qu'ils sont connectés dans le graphe

Une chaîne est dite ==simple== si elle ne passe pas 2 fois par la même arrête.
Une chaîne est dite ==élémentaire== est une chaîne simple qui ne passe pas deux fois par le même sommet

**Remarque**: Toute chaîne contient une chaîne élémentaire de même extrémités.