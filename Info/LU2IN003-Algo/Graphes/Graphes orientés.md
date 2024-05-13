#algo
# Définition
On qualifie un graphe orienté $G$ le couple $(V, A)$ où $V$ est un ensemble de sommets et $A$ un ensemble d'arcs. A la différence d'un [[Graphes non orientés]], l'ensemble $A$ est un couple de sommet, l'ordre a donc une importance.

On dit qu'un graphe orienté est ==connexe== si le [[Graphes non orientés]] sous-jacent est lui même connexe.

# Terminologie

Soit un graphe orienté $G = (V, A)$ on note:
- $\Gamma^+(u) = \set{v \in V, (u,v) \in A}$ les successeurs de $u$
- $\Gamma^-(u) = \set{v \in V, (v,u) \in A}$ les prédécesseurs de $u$
- Un chemin est une séquence de sommets et d'arcs $v = v_1e_1\cdots e_nv_{n+1}$ 

Naturellement on définie les $\frac{1}{2}$-degré le cardinal de l'ensemble des successeurs et des prédécesseurs. Le degré est la somme des $\frac{1}{2}$ degré

# Arborescence
Un graphe orienté $\mathcal{A} = (V, A)$ est une arborescence si on peut l'obtenir à partir d'un arbre en orientant les arêtes de sortes qu'il y ait une racine.
Pour en construire à partir d'un graphe orienté quelconque, on choisit un sommet, et on réoriente les arêtes arrivante en arêtes incidente

# Matrices sommets-arcs
On note $R$ une matrice $|V| \times |A|$ telle que, $\forall(i,j) \in V \times A$ on a:
- $R_{ij} \in \set{-1, 0, 1}$
Une case de cette matrice vaut $-1$ si l'arcs part du sommet en question, et $1$ si l'arc arrive sur le sommet en question

# Matrices sommets-sommets
On note $R$ une matrice $|V|^2$ telle que $\forall(i,j) \in V^2$
- $R_{ij} = \set{0, 1}$
Une case vaut 1 si un arc connecte 2 sommets entre eux. Il se lit de la ligne vers la colonne:
S'il y a 1 en 2, 3: alors il y a un arc $(2, 3)$
S'il y a 1 en 3, 2: alors il y a un arc $(3, 2)$

# Composantes fortement connexe
On parle de composantes fortement connexe s'il existe un chemin relient un sommet $u$ vers un sommet $v$ et un autre chemin liant $v$ avec $u$

# Définition de la racine
Une racine dans un graphe orienté est un sommet dans lequel on peut atteindre tous les autres sommets du graphe.
Soit alors pour $G = (V, E)$ on a $v \in V$ une racine si et seulement si  $\forall u \in V\setminus \{v\}$ un chemin existe entre $v$ et $u$

# Rang d'un sommet
On définit le rang d'un sommet $u$ comme suit:
$$rang(u)\begin{cases}0  \text{ si }\Gamma^-(u) = \emptyset \\
1 + \max\{rang(v) \: | \: v \in \Gamma^-(u)\}\end{cases}$$

## Tri topologique
### Définition
On définit un tri topologique de $G$, un graphe orienté sans circuit come étant une liste de sommet $(u_1, \dots, u_n)$ de sommets de $G$ telle que:
$\forall i < j$ il n'existe aucun chemin de $u_j$ à $u_i$

### Lemme lien entre tir topologique et rang de sommet
Pour tout graphe non orientés sans circuit à $n$ sommets
- Il existe $u_1, \dots, u_n$ des sommets distincts tel que: $rang(u_1) \leq \dots \leq rang(u_n)$
- Si $rang(u_1) \leq \dots \leq rang(u_n)$ alors $(u_1, \dots, u_n)$ est un tri topologique.
	==**ATTENTION**==: La réciproque du deuxième point n'est pas vraie en tout temps
