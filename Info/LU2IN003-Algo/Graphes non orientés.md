#algo

Un [[Graphes]] est dit non orienté, si toutes ses arêtes connectent les sommets dans les 2 sens.

## Chaînes particulières

On définit un ==cycle==, une chaîne fermée (i.e tel que $v_{n+1} = v_1$)
Un cycle est dit ==élémentaire== s'il s'agit d'une [[Graphes#Chaîne|chaîne élémentaire]] fermée

Un graphe non orienté est dit ==connexe== s'il existe pour tout couple de sommet $(v, u) \in V^2$, une chaîne élémentaire entre $u$ et $v$ (i.e, [[Graphes#Chaîne|rappellons le]], il existe une connexion entre un sommet et un autre, même indirect)

### Composantes connexes
On appelle composantes connexes, l'ensemble des sommets de $G$ induisant $SG$, un sous graphe connexe.

## Degré d'un sommet
Soit $G = (V, E)$, un graphe non orienté.
On définit le degré d'un sommet $v$, l'élément:
$$d(v) = |\Gamma(v)|$$
### Théorème
Pour tout graphe $G = (V, E)$ non orienté; $\sum_{v \in V} d(v) = 2|E|$

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

## Théorème d'Euler sur les graphes connexe

Soit $G$ un graphe connexe
- Si tous les sommets de $G$ ont un degré pair, alors il existe un circuit eulérien: (On passe par tous les sommets du graphes, sans repasser 2 fois par la même arrête)
- Si tous les sommets sauf 2 ont un degré pair, il existe un chemin eulérien entre les 2 sommets impair
- S'il y a 4 sommets ou plus de degrés impaires, il n'y a ni circuit, ni chemin eulérien.