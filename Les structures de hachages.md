#struct 
Afin de pouvoir associer des éléments à des clefs, comme des [[Dictionnaires]]. Il est nécessaire de manipuler le hachage.

Le concept est d'associer à une clef (une chaîne de caractère en général) à un entier.

Une **Table de hachage** associe à une chaîne de caractère une valeur; Chaque indice de cette table correspond au résultat de la fonction hachage. 
Attention néanmoins, il peut exister des collisions qu'il faudra résoudre !

## Fonctions de hachage
Une fonction de hachage est de la forme $h: U \to \set{1, \cdots, n}$ où $U$ représente l'univers des clé et $\set{1, ..., n}$ l'ensemble des indices sur le tableau.

**Important**: Une fonction de hachage doit avoir une complexité de $O(1)$

Si le nombre de case du tableau est au moins proportionnel au nombre d'éléments à stocker: $\alpha = \frac{n}{m} = O(m)/m = O(1)$ C'est le facteur de charge.
Dans ce cas, l'ajout, la recherche d'éléments et la suppression dans les listes doublement chaînée est en $O(1)$

Ces fonctions peuvent créer de la superposition.

*Exemple:*
On pose $h(k) = k\%7$

Une bonne fonction de hachage est de complexité $O(1)$ et minimise les collisions

### Contrer la collision
Plusieurs clé auront la même valeur de hachage, pour remédier à ce problème, il est courant d'utiliser une liste chaîné qui associe à la valeur de k, la nouvelle clé concernée.

Il est aussi possible d'utiliser la méthode d'adressage ouvert. Cette fois-ci, notre fonction de hachage prend deux paramètres. On parcours le tableau jusqu'à ce qu'une case soit vide. Cette méthode s'appelle le double hachage.
