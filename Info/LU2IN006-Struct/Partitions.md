## Définition
On définit une partition de la façon suivante: #!

Un partition de $X$ est un ensemble de sous-ensembles de $X$, deux à deux disjoints, et dont l'union est égale à $X$. Chaque sous-ensemble de la partition est communément appelé *"classe d'équivalence"* et on choisit arbitrairement un de ses éléments pour la représenter.
On souhaite avoir les opérations classiques:
- `CreerClasse(x)` qui créer la classe d'équivalence dont le représentant est $x \in X$
- `Union(x, y)` qui joint les classes d'équivalence représentée par $x$ et $y$
- `Find(x)` qui renvoie le représentant de la classe contenant $x$

### Exemple, les composantes connexes
Dans un graphe non orienté, une composante connexe est un sous graphe induit maximal connexe. 
Les composantes connexes définissent une partition de l'ensemble des sommets


## Implémentations

### En table de hachage
On peut implémenter une partition à l'aide d'une [[Table de hachage]] qui à tout élément, associe un entier désignant le numéro de sa classe d'équivalence.![[Pasted image 20240509201219.png]]

#### Complexité
Avec une implémentation par table de hachage on observe les complexités suivantes pour une structure de partition: #!

- `Find(x)` est en $O(1)$ car il suffit d'accéder à la bonne case de la table de hachage
- `Union(x, y)` est en $O(n)$ car il faut parcourir toute la table pour trouver les éléments qui doivent changer de classe d'équivalence


### En liste de liste chaînées
On peut implémenter une partition à l'aide d'une liste de liste chaînées dont chaque sous liste contient les éléments d'une classe d'équivalence.

#### Complexité
Avec une implémentation par liste de liste chaînées on observe les complexités suivantes pour une structure de partition: #!

- `Find(x)` est en $O(n)$ car il est nécessaire de parcourir l'intégralité des éléments de chaque classe d'équivalence pour trouver $x$
- `Union(x, y)` est en $O(1)$ car on concatène juste les deux listes entre elles.

### En forêt
C'est la représentation la plus optimal, on aura alors un groupe d'arbre que l'on appelle forêt, où chaque arbre est une classe d'équivalence, et où la forêt est la partition.

A noter qu'une forêt n'est optimale que si les arbres sont équilibrés, on étudie alors la méthode suivante:

#### Union-find, implémentation optimale de la forêt.
Pour représenter une partition en forêt de façon optimale, on utilise le principe d'union-find: #!

Lorsque l'on exécute `Find(x)` l'idée est de profiter de cet appel pour connecter tous le chemins nécessaire pour remonter de $x$ jusqu'à la racine de l'arbre, pour connecter tous les nœuds à la racine de l'arbre
Lorsque l'on fait une union, on utilise l'*union par rang*. On stocke alors le rang (le rang d'un arbre avec un seul nœud est de 1) de chaque arbre de la forêt, et lors d'une union, la racine de l'arbre avec le plus grand rang devient père de la racine de l'arbre avec le plus petit rang. Le rang de l'arbre obtenu est donc le plus grand rang des deux. Si les rangs sont les mêmes, le choix est arbitraire et l'arbre résultant voit son rang incrémenté de 1

#### Implémentation optimale
```c
typedef struct s_noeud {
	int elem;
	int rang;
	struct s_noeud* pere;
} Noeud;

Noeud* creerClasse(int elem) {
	Noeud* n = (Noeud*) malloc(sizeof(Noeud));
	n->elem = elem;
	n->rang = 1;
	n->pere = n;
	return n;
}

Noeud* find(Noeud* n) {
	if(n->pere != n) {
		n->pere = find(n);
	} 
	return n->pere;
}

void union(Noeud* n1, Noeud* n2) {
	Noeud* r1 = find(n1);
	Noeud* r2 = find(n2);

	if(r1 == r2) return;
	(r2->rang > r1->rang) ? r1->pere = r2 : r2->pere = r1;
	if(r1->rang == r2->rang) r1->rang++;
}
```