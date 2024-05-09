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