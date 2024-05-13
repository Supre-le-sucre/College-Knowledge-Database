#algo 
# Comparaison
Un algorithme de tri est dit de comparaison s'il compare les éléments deux à deux pour les trier

## Complexité minimale
Un algorithme de tri de comparaison à un complexité minimal de $O(nlog(n)$) dans le pire cas.

En effet, s'il l'on fait au plus $n$ comparaisons, on peut renvoyer au plus $2^n$ valeurs diférentes. Une liste a $n!$ permutations possibles avec $n! > 2^n$. Dans le pire cas, il faut un nombre $k$ de comparaison tel que: $2^k > n!$
D'où cette complexité minimale.

# Stable
Un algorithme de tri est dit stable s'il n'inverse pas l'ordre de deux éléments de même clef.

Par exemple: Trier les étudiants seront leur notes les affichera dans l'autre alphabétique s'ils ont la même note.

### Exemple tri par insertion
Le tri par insertion consiste à ajouter un élément à une liste, puis trier la liste en conséquence. Ce tri est dit *stable*. Dans le meilleur des cas, le tableau initial est déjà trié, et sa complexité est donc $\Omega(n)$. Autrement, sa complexité est de $\mathcal{O}(n^2)$ dans le pire des cas.

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

# En place
un algorithme de tri est dit en place s'il ne nécessite pas de dupliquer une partie des éléments une partie des éléments à trier 
