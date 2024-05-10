Une file de priorité est une [[Files]], qui n'est pas FIFO, mais qui fait sortir les éléments prioritaire en premier, puis le reste en FIFO.

## Définition
On définit une file de priorité de la façon suivante: #!

Ce type de données représente un ensemble de données homogène chacune associée à une valeur, son niveau de priorité. Une file de priorité permet l'extraction d'élément de priorité minimal ou maximal et l'ajout aisé de nouvelles données.
On tient à avoir ces opérations classiques:
- `Ajouter(x, p, F)` ajoute $x$ avec une priorité $p$ à la file $F$
- `ExtraireMin(F)` sort l'élément avec la plus petit priorité de $F$
- `Fusionner(F1, F2)` fusionne les files $F_1$ et $F_2$ 

## Implémentations

### En tableau
On peut implémenter une file de priorité par un tableau. Chaque case contient un élément de la file de priorité. Il peut éventuellement être trié par ordre de priorité.

#### Complexité
Pour une file de priorité avec une représentation en tableau, on observe les complexités suivantes: #!

- `Ajouter(x, p, F)` est en $O(1)$ si le tableau n'est pas trié. Si le tableau est trié en revanche, elle sera en $O(n)$ car il est nécessaire de le parcourir en entier pour placer, et déplacer les éléments au besoin
- `ExtraireMin(F)` est en $O(n)$ pour un tableau non trié, cas parcourir tout le tableau est nécessaire. En revanche elle est en $O(1)$ dans le cas trié
- `Fusionner(F1, F2)` est en $O(n_1 + n_2)$ qu'il soit trié ou non, car il faut recréer un tableau puis parcourir les deux tableaux en même temps pour les intercaler efficacement.

### En [[Arbres AVL]]
On peut implémenter une liste de priorité en [[Arbres AVL]] où chaque nœud de l'arbre correspond à un élément de la fil de priorité et où les clés sont les niveaux de priorité de chaque élément.

#### Complexité
Pour une représentation en [[Arbres AVL]] d'une file de priorité, on observe les complexités suivantes: #!

- `Ajouter(x, p, F)` est en $O(log(n))$ car la hauteur d'un arbre AVL est de l'ordre logarithmique
- `ExtraireMin(F)` est en $O(\log(n))$ car le minimum est la feuille la plus à gauche
- `Fusionner(F1, F2)` est en $O(n_1 + n_2)$ car on reconstitue les arbres en liste, et on recréer le nouvelle arbre AVL (cf. [[Ensembles#En Arbres AVL|Complexité de unir]])

### En [[Tas binomial]]
On peut implémenter une file de priorité en [[Tas binomial]], chaque élément du tableau est donc un élément avec sa priorité.

#### Complexité
Pour une représentation en [[Tas binomial]] d'une file de priorité, on observe les complexités suivantes: #!

- `Fusion(F1, F2)` est en $O(\log(n))$ (cf.[[Tas binomial]])
- `Ajouter(x, p, F)` est en $O(\log(n))$ car on créer un tas binomial contenant uniquement l'élément à ajouter $x$ que l'on fusionne au tas courant
- `ExtraireMin(F)` car il s'agit de trouver la racine parmi $\log(n)$ arbre binomiaux
**Remarque**: Sous forme de tas binomial, on peut aussi augmenter et diminuer la priorité d'une clé quelconque en $O(\log(n))$. 
