#algo 
# Comparaison
On définit le tri par comparaison de la façon suivante: #!

Un algorithme de tri est dit de comparaison s'il compare les éléments deux à deux pour les trier
<!--ID: 1715690724128-->


## Complexité minimale
Un algorithme de tri de comparaison a une complexité minimale de: #!

$O(nlog(n)$) dans le pire cas. En effet, s'il l'on fait au plus $n$ comparaisons, on peut renvoyer au plus $2^n$ valeurs différentes. Une liste a $n!$ permutations possibles avec $n! > 2^n$. Dans le pire cas, il faut un nombre $k$ de comparaison tel que: $2^k > n!$
D'où cette complexité minimale.
<!--ID: 1715690724129-->


# Stable
On dit qu'un algorithme de tri est stable lorsque: #!

Celui-ci n'inverse pas l'ordre de deux éléments de même clef.
Par exemple: Trier les étudiants seront leur notes les affichera dans l'autre alphabétique s'ils ont la même note.
<!--ID: 1715690724131-->


# En place
un algorithme de tri est dit en place s'il #!
ne nécessite pas de dupliquer une partie des éléments une partie des éléments à trier 
<!--ID: 1715690724133-->

