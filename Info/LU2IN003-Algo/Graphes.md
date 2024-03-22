## Définition
Un graphe est un couple entre un ensemble de sommets $V$ (pour vertex) et un ensemble d'arrêtes $E$ (pour edge) qui est une paire de sommet. On note $G = (V, E)$

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

### Preuve
Posons $\Pi(n):$ "Toute chaîne de longueur $n$ contient une chaîne élémentaire de même extrémités"

(B): Une chaîne de longueur $0$ est déjà élémentaire

(H): Soit $\forall k < n \in \Pi(k)$ vraie, montrons $\Pi(n)$:

Soit $C$ une chaîne de longueur $n$
Si $C$ est déjà une chaîne élémentaire, alors c'est trivial.

Sinon, on note $C = v_0e_1v_1e_2v_2\dots e_nv_n$ et il existe $i < j$ tel que $v_i = v_j$
On pose $C' = v_0e_1v_1\dots e_iv_ie_{j+1}v_{j+1}\dots e_nv_n$

On obtient alors une chaîne de même extrémités que $C$ et de longueur $k = n-j+1 <n$
D'après $\Pi(k)$ on peut extraire de $C'$, une chaîne élémentaire de mêmes extrémités de $C'$ donc que de $C$
$$\tag*{$\blacksquare$}$$
