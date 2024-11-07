# Définition
On définit le tri par insertion de la manière suivante: #!

Le tri par insertion consiste à ajouter un élément à une liste, puis trier la liste en conséquence. Ce tri est dit [[Algorithme de tri#Stable|stable]]. 
<!--ID: 1715690724114-->


## Complexité
La complexité du tri par insertion est la suivante: #!

Dans le meilleur des cas, le tableau initial est déjà trié, et sa complexité est donc $\Omega(n)$Autrement, sa complexité est de $\mathcal{O}(n^2)$ dans le pire des cas.
<!--ID: 1715690724115-->


## Implémentation
On implémente le tri par insertion de la manière suivante:

```python
def insertionElem(tab, j):
	tmp = tab[j]
	i = j-1
	while i > -1 and tab[i] > tmp:
		tab[i+1] = tab[i]
		i = i - 1
	tab[i+1] = tmp
```

```python
def insertionSort(tab):
	j = 1
	n = len(tab)
	while j != n:
	# inserer tab[j] dans tab[0...j-1]
	# a sa place
		insertionElem(tab, j)
		j = j + 1
```

Son avantage est donc d'aller très vite dans les listes déjà plutôt bien triée.
