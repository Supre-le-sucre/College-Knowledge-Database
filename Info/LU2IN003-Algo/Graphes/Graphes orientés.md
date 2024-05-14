#algo
# Définition
On qualifie un graphe orienté $G$ #!
Le couple $(V, A)$ où $V$ est un ensemble de sommets et $A$ un ensemble d'arcs. A la différence d'un [[Graphes non orientés]], l'ensemble $A$ est un ==couple== de sommet, l'ordre a donc une importance.
<!--ID: 1715702538671-->



# Terminologie

## Successeurs et prédécesseurs
Soit un graphe orienté $G = (V, A)$ on note: #!

- $\Gamma^+(u) = \set{v \in V, (u,v) \in A}$ les successeurs de $u$
- $\Gamma^-(u) = \set{v \in V, (v,u) \in A}$ les prédécesseurs de $u$
<!--ID: 1715702538674-->


### $\frac{1}{2}$-degré
Naturellement on définie les $\frac{1}{2}$-degré: #!
Le cardinal de l'ensemble des successeurs et des prédécesseurs. Le degré est la somme des $\frac{1}{2}$-degré
<!--ID: 1715702538676-->


## Chemin
On définit dans un graphe orienté un chemin comme suit: #!

- Un chemin est une séquence de sommets et d'arcs $v = v_1e_1\cdots e_nv_{n+1}$ 
- Un chemin élémentaire est un chemin qui ne passe pas 2 fois par le même sommet
<!--ID: 1715702538679-->


### Circuit
Un circuit est défini de la façon suivante: #!

- Un circuit est un chemin $\gamma$ tel que $v_{n+1} = v_1$
- Un circuit élémentaire est un chemin élémentaire tel que $v_{n+1} =v_1$
<!--ID: 1715702538681-->


# Connexité

## Graphe orienté connexe
On dit qu'un graphe orienté est ==connexe== si #!
Le [[Graphes non orientés]] sous-jacent est lui même connexe.
<!--ID: 1715702538683-->


## Composantes fortement connexe
Dans un graphe orienté, on parle de composantes fortement connexe #! 
S'il existe un chemin relient un sommet $u$ vers un sommet $v$ et un autre chemin liant $v$ avec $u$
<!--ID: 1715702538686-->


### Relation fortement connexe
On peut observer le résultats suivant: #!

Soit $\mathcal R$ la relation de forte connexité sur l'ensemble $V^2$. On a donc $u \mathcal R v$ si et seulement si $u$ et $v$ sont fortement connexe (donc il existe un chemin entre $u$ et $v$ et de $v$ jusqu'à $u$).
- La relation de forte connexité est une [[Relations d'équivalence]].
- Les classes d'équivalence de cette relation sont les [[#Composantes fortement connexe]] de $G$
- Un graphe est fortement connexe si la relation de forte connexité ne possède qu'une seule classe d'équivalence
<!--ID: 1715702538688-->


# Définition de la racine
Une racine $r$ dans un graphe orienté est un sommet tel que: #!
A partir du sommet $r$ on peut atteindre tous les autres sommets du graphe.
Soit alors pour $G = (V, A)$ on a $v \in V$ une racine si et seulement si  $\forall u \in V\setminus \{v\}$ un chemin existe entre $v$ et $u$
<!--ID: 1715702538691-->


## Arborescence
Un graphe orienté $\mathcal{A} = (V, A)$ est une arborescence si #!
Il existe une racine dans $\mathcal A$, autrement dit, s'il existe un sommet par lequel on peut atteindre tous les autres
<!--ID: 1715702538693-->


# Relation d'ordre de base
On définit pour tout graphe orienté $G = (V, A)$ ==sans circuit== la relation d'ordre suivante: #!
On a que $u \leq v$ si et seulement si il existe un chemin allant de $u$ vers $v$ dans $G$
<!--ID: 1715702538695-->


## Remarques importantes
Pour définir la relation d'ordre $\leq$ dans un graphe orienté $G$ plusieurs éléments sont à prendre en compte: #!

- Pour que la relation d'ordre soit antisymétrique, le graphe doit être ==sans circuit==
- l'ordre $\leq$ peut être total ou partiel (ça dépend de la connexité)
# Rang d'un sommet
On définit le rang d'un sommet $u$ comme suit: #!
$$rang(u)\begin{cases}0  \text{ si }\Gamma^-(u) = \emptyset \\
1 + \max\{rang(v) \: | \: v \in \Gamma^-(u)\}\end{cases}$$ Remarquons que cette définition n'a de sens que si $G$ est un graphe sans circuit
<!--ID: 1715702538698-->


## Tri topologique
### Définition
On définit un tri topologique de $G$, un graphe orienté ==sans circuit==, comme étant une liste de sommet $(u_1, \dots, u_n)$ de sommets de $G$ telle que: #!
$\forall i < j$ il n'existe aucun chemin de $u_j$ à $u_i$
<!--ID: 1715702538700-->


### Lemme lien entre tir topologique et rang de sommet
Pour tout graphe non orientés sans circuit à $n$ sommets #!
- Il existe $u_1, \dots, u_n$ des sommets distincts tel que: $rang(u_1) \leq \dots \leq rang(u_n)$
- Si $rang(u_1) \leq \dots \leq rang(u_n)$ alors $(u_1, \dots, u_n)$ est un tri topologique.
	==**ATTENTION**==: La réciproque du deuxième point n'est pas vraie en tout temps
<!--ID: 1715702538703-->


### Tri topologique avec le rang
On peut définir un tri topologique en utilisant le rang d'un sommet: #!

Si on range les sommets dans l'ordre croissant de leur rang, alors on obtient un tri topologique
<!--ID: 1715702538705-->
