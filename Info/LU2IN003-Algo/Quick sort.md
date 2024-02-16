#algo
Le Quick sort est l'[[Algorithme de tri]] le plus répandu et le plus rapide, sa complexité étant $\mathcal O(nlog(n))$.
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