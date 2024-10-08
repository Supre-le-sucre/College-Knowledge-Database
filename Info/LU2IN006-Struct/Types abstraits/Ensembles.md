## Définition
On définit la structure de donnée ensembliste de la façon suivante: #!

Elle représente un ensemble fini d'élément. Il ne devrait pas y avoir plusieurs fois le même élément. Il faut donc introduire la notion d'égalité entre les éléments. On considère les opérations classiques entre les éléments:
<!--ID: 1715341583436-->


- `Vérifier(x, S)` vérifie la présence de l'élément $x$ dans $S$
- `Insérer(x, S)` insère $x$ dans $S$
- `Supprimer(x, S)` supprime $x$ de $S$
- `Intersecter(S, T)` calcul l'intersection les ensembles $S$ et $T$
- `Unir(S, T)` calcul l'union des ensembles $S$ et $T$

## Implémentations

### En liste chaînée
Un ensemble peut être implémenté comme une liste chaînée, les éléments qui la compose sont donc les éléments de l'ensemble.

#### Complexité
On observe les complexités suivantes pour un ensemble implémenté en liste chaînée: #!

- `Verifier(x, S)` est en $O(n)$ car il faut dans le pire cas parcourir toute la liste
- `Inserer(x, S)` est en $O(n)$ car on souhaite maintenir l'intégrité de l'ensemble, et donc vérifier si $x$ n'est pas déjà dans $S$
- `Supprimer(x, S)` est en $O(n)$ car dans le pire cas, l'élément $x$ n'est pas dans $S$
- `Intersecter(S, T)` et `Unir(S, T)` sont en $O(n_S \times n_T)$ car il faut comparé deux à deux tous les éléments de la liste. La complexité passe à $O(\max\{n_S\log(n_S), n_T\log(n_T)\})$ si les éléments sont triés, car on procède en dichotomie
<!--ID: 1715341583439-->


### En [[Table de hachage]]
On peut représenter un ensemble en [[Table de hachage]] pour une taille $m$ fixé. Chaque élément $e$ de l'ensemble $S$ se trouvent alors à la position $h(e)$ du tableau.

En pratique cet implémentation est la plus efficace pour effecteur l'ensemble de ces opérations. Cependant quand les éléments peuvent être ordonnés et qu'il doivent être parcouru dans l'ordre, cet structure empêche de le conserver

#### Complexité
On observe les complexités suivantes pour un ensemble implémenté en [[Table de hachage]]: #!

- `Vérifier(x, S)`, `Insérer(x, S)` et `Supprimer(x, S)` sont en $O(1)$ pour une taille de table de hachage optimale et sans collision.
- `Intersecter(S, T)` et `Unir(S, T)` sont en $O(m)$ où $m$ la taille de la table de hachage. Car elle demandent de comparer la table de hachage case par case.
<!--ID: 1715341583441-->


### En [[Arbres AVL]]
On peut représenter un ensemble en un [[Arbres AVL]] (ou un équivalent) dont les nœuds correspondent donc aux éléments de l'ensemble.

#### Complexité
On observe les complexités suivantes pour un ensemble implémenté en [[Arbres AVL]]: #!

- `Vérifier(x, S)`, `Insérer(x, S)` et `Supprimer(x, S)` sont en $O(\log(n))$ car sa hauteur est de l'ordre logarithmique
- `Intersecter(S, T)` et `Unir(S, T)` sont en $O(n_S + n_T)$. On créer un tableau trié à partir de chaque AVL (donc $O(n)$) puis on les parcourt en même temps pour créer le tableau trié contenant les élément de l'arbre AVL retourné (en $O(n_S + n_T)$). Par dichotomie, l'arbre AVL peut-être construit en $O(n_S + n_T)$, la racine de l'arbre AVL étant le milieu du tableau puis récursivement, chaque autre moitié devenant une sous racine...
- `Parcourir(S)` est en $O(n)$ car il suffit de faire un parcours infixe de l'arbre pour afficher les éléments dans l'ordre.
<!--ID: 1715341583444-->
