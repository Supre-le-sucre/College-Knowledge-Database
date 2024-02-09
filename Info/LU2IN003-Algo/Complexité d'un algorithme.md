#algo
## Définition
La complexité d'un algorithme est une évaluation du nombre d'instruction élémentaire lors de l'exécution de l'algorithme.
Il ne s'agit pas de faire un comptage précis selon les paramètres, mais de faire une approximation avec les [[La notation de Landau]].

## Complexité pire et meilleur cas
L'évaluation de la complexité dépend du paramètre fourni à l'algorithme. 
On peut évaluer la complexité dans le pire des cas, donc la borne supérieur (c'est en général celle qu'on utilise pour étudie un algorithme).
Mais il est aussi possible d'évaluer le meilleur cas.

*Exemple*: Lorsqu'on recherche un élément dans le tableau...
- Le meilleur des cas est $\Omega(1)$, l'élément est à la première cas du tableau.
- Le pire des cas est $O(n)$, l'élément n'est pas dans le tableau.

**ATTENTION**: La complexité est asymptotique, lorsque l'on étudie, c'est lorsque $n$ est grand. Il est absurde de justifier une complexité en fonction de la taille de $n$