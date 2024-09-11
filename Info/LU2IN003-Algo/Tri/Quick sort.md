#algo

# Définition
Le Quick sort est l'[[Algorithme de tri]] le plus répandu. #!
L'objectif est d'avoir un pivot au milieu de chaque listes est de trier les sous listes ensembles dépendant du pivot. Le quick sort n'est pas [[Algorithme de tri#Stable|stable]] car il permutera les éléments ayant la même clé.
<!--ID: 1715690724117-->


## Implémentation
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
On définit la fonction d'éclatement telle que: #!

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
<!--ID: 1715690724119-->


## Complexité
La complexité du quick sort est donné de la façon suivante: #!
- La complexité de l'éclatement est en $\Theta(n)$.
- Dans le meilleur des cas, le quick sort aura une complexité de $\Omega(nlog(n))$
- Mais dans le pire des cas, sa complexité sera de $\mathcal O(n^2)$: 
	C'est lorsque le pivot est le plus grand ou le plus petit élément de la liste. Etonnement donc, le pire cas n'arrive que lorsque la liste est triée !
	Pour éviter un tel phénomène, on pourrait prendre comme pivot, un élément au milieu de la liste.
	Mais ce pire cas existerait toujours si la liste était formée de tel sorte à ce que l'élément du milieu soit toujours le plus grand (ou le plus petit).
<!--ID: 1715690724120-->


## Exemple d'arbre d'exécution du quick sort
L'arbre d'exécution du quick sort pour la liste `[12, 2, 17, 25, 7, 5]` est le suivant (le pivot est le première élément de la liste traitée): #!
![[Pasted image 20240514131122.png]]
<!--ID: 1715690724122-->


