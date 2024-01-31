#struct 
Afin de pouvoir associer des éléments à des clefs, comme des [[Dictionnaires]]. Il est nécessaire de manipuler le hachage.

Le concept est d'associer à une clef (une chaîne de caractère en général) à un entier.

Une **Table de hachage** associe à une chaîne de caractère une valeur; Chaque indice de cette table correspond au résultat de la fonction hachage. 
Attention néanmoins, il peut exister des collisions qu'il faudra résoudre !

## Fonctions de hachage
Une fonction de hachage est de la forme $h: U \to \set{1, \cdots, n}$ où $U$ représente l'univers des clé et $\set{1, ..., n}$ l'ensemble des indices sur le tableau.

Ces fonctions peuvent créer de la superposition.

*Exemple:*
On pose $h(k) = k\%7$
Plusieurs clé auront la même valeur de hachage, pour remédier à ce problème, il est courant d'utiliser une liste chaîné qui associe à la valeur de k, la nouvelle clé concernée.