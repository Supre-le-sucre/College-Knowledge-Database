#algo
Le Quick sort est l'[[Algorithme de tri]] le plus répandu.
L'objectif est d'avoir un pivot au milieu de chaque listes est de trier les sous listes ensembles dépednant du pivot.

L'algorithme est récursif et se construit de la façon suivante:
```python 
def Quicksort(L):
	if (len(L)>1):
		L1=[] ; L2=[] ; L3=[]
		L3.append(L[0])
		Eclatement(L, L1, L2)
		return Quicksort(L1)+L3+Quicksort(L2)
	return L
```

La fonction d'éclatement sépare la liste `L` en deux sous liste, les éléments plus petit que le pivot `L[0]` vont en `L1`, les éléments plus grand vont en `L2`
```python
def Eclatement(L, L1, L2):
	x=L[0]
	for y in L[1:]:
		if (y<x):
			L1.append(y)
		else:
			L2.append(y)
```

## Complexité

La complexité de l'éclatement est en $\Theta(n)$.
Dans le meilleur des cas, le quick sort aura une complexité de $\Omega(nlog(n))$

Mais dans le pire des cas, sa complexité sera de $\mathcal O(n^2)$: C'est lorsque le pivot est le plus grand ou le plus petit élément de la liste. Etonnement donc, le pire cas n'arrive que lorsque la liste est triée !
Pour éviter un tel phénomène, on pourrait prendre comme pivot, un élément au milieu de la liste.

Mais ce pire cas existerait toujours si la liste était formée de tel sorte à ce que l'élément du mileiu soit toujours le plus grand (ou le plus petit).