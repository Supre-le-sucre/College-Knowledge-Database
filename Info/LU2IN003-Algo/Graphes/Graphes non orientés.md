#algo 
## Définition
Un graphe non orienté est: #!
Un couple entre un ensemble de sommets $V$ (pour vertex) et un ensemble d'arrêtes $E$ (pour edge) qui est une paire de sommet. On note $G = (V, E)$
<!--ID: 1715702538708-->


## Voisins
On appelle les voisins (ou sommets adjacents) d'une arrête $v$, l'ensemble de sommets notés $\Gamma(v)$ définie tel que: #!
$$\Gamma(v) = \set{v' \; | \; \set{v', v} \in E}$$
<!--ID: 1715702538711-->


## Degré d'un sommet
Soit $G = (V, E)$, un graphe non orienté.
On définit le degré d'un sommet $v$, l'élément: #!
$$d(v) = |\Gamma(v)|$$
### Théorème
Pour tout graphe $G = (V, E)$ non orienté on observe le phénomène suivant liant le degré de chaque sommet et le nombre d'arêtes: #!
$$\sum_{v \in V} d(v) = 2|E|$$
<!--ID: 1715702538713-->


#### Preuve
On pose $\Pi(n):$ "Si un graphe a $n$ arêtes, alors la somme des degrés est $2n$"

(B): Si un graphe n'a pas d'arête, alors tous les sommets sont de degré $0$ OK.

(H): Soit $n \in \mathbb N, \Pi(n)$ vraie, montrons $\Pi(n+1)$
Soit $G$ un graphe avec $n+1$ arêtes. Soit $\set{u, v}$ une arête de $G$, on pose $H$ le sous graphe de $G$ obtenu en retirant l'arête $\set{u,v}$.

Observons: 
$\forall x \not \in \set{u,v}, d_H(x) = d_G(x)$
$d_H(u) = d_G(u) -1$ et $d_H(v) = d_G(v) -1$

On a que
$$\sum_{x \in V} deg_G(x) = \sum_{x \in V\setminus\set{u,v}} deg_G(x) + deg_G(u) + deg_G(v)$$
$$= \sum_{x \in V\setminus\set{u,v}} deg_H(x) + deg_H(u) + deg_H(v) + 2$$
$$= \sum_{x \in V} deg_H(x) + 2$$
$$= 2n +2 = 2(n+1)$$
$$\tag*{$\blacksquare$}$$


## Chaîne
Une chaîne est définie tel que: #!
Un chaîne est une séquence de sommets et d'arrêtes tels qu'ils sont connectés dans le graphe
- Une chaîne est dite ==simple== si elle ne passe pas 2 fois par la même arrête.
- Une chaîne est dite ==élémentaire== est une chaîne simple qui ne passe pas deux fois par le même sommet
**Remarque**: Toute chaîne simple peut être transformée en chaîne élémentaire de même extrémités.
<!--ID: 1715702538715-->


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

## Cycles
On définit un ==cycle== de la façon suivante: #!
Un cycle est une [[#Chaîne]] fermée (i.e tel que $v_{n+1} = v_1$)
Un cycle est dit ==élémentaire== s'il s'agit d'une chaîne ==élémentaire== fermée
<!--ID: 1715702538718-->


### Maximal acyclique
On dit d'un [[Graphes non orientés]] qu'il est maximal acyclique si $G$ est sans cycle élémentaire, mais que rajouter une nouvelle arête entraîne la création d'un cycle.
(i.e pour tout couple de sommets $\set{x, y}$ non adjacents dans $G$. On a que $G' = (V, E \cup \set{\set{x, y}}$ contient un cycle)

## Connexité 
Un graphe non orienté est dit ==connexe== #!
S'il existe pour tout couple de sommet $(v, u) \in V^2$, une [[#Chaîne]] élémentaire entre $u$ et $v$ 
<!--ID: 1715702538720-->


### Composantes connexes
On appelle composante connexes, l'ensemble des sommets $V_C$ d'un graphe $G$ tel que: #!
Le [[Sous graphes#Graphes induits|graphe induit]] par $V_C$ est connexe
<!--ID: 1715702538722-->


### Minimal connexe
On dit d'un [[Graphes non orientés]] qu'il est minimal connexe s'il est connexe, et que si l'on retire n'importe quel arête du graphe, il n'est plus connexe (i.e $\forall e \in E, G' = (V, E-\set{e})$ non connexe)

## Théorème d'Euler sur les graphes connexe
Soit $G$ un graphe connexe: #!

- Si tous les sommets de $G$ ont un degré pair, alors il existe un circuit eulérien: (On passe par tous les sommets du graphes, sans repasser 2 fois par la même arrête)
- Si tous les sommets sauf 2 ont un degré pair, il existe un chemin eulérien entre les 2 sommets impair
- S'il y a 4 sommets ou plus de degrés impaires, il n'y a ni circuit, ni chemin eulérien.
$$\tag*{$\blacksquare$}$$
<!--ID: 1715702538725-->



