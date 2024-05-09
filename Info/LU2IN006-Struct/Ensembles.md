## Définition
On définit la structure de donnée ensembliste de la façon suivante: #!

Elle représente un ensemble fini d'élément. Il ne devrait pas y avoir plusieurs fois le même élément. Il faut donc introduire la notion d'égalité entre les éléments. On considère les opérations classiques entre les éléments:

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

### En table de hachage
On peut représenter un ensemble en table de hachage pour une taille $m$ fixé. Chaque élément $e$ de l'ensemble $S$ se trouvent alors à la position $h(e)$ du tableau.

En pratique cet implémentation est la plus efficace pour effecteur l'ensemble de ces opérations. Cependant quand les éléments peuvent être ordonnés et qu'il doivent être parcouru dans l'ordre, cet structure empêche de le conserver

#### Complexité
On observe les complexités suivantes pour un ensemble implémenté en table de hachage: #!

- `Vérifier(x, S)`, `Insérer(x, S)` et `Supprimer(x, S)` sont en $O(1)$ pour une taille de table de hachage optimale et sans collision.
- `Intersecter(S, T)` et `Unir(S, T)` sont en $O(m)$ où $m$ la taille de la table de hachage. Car elle demandent de comparer la table de hachage case par case.

E