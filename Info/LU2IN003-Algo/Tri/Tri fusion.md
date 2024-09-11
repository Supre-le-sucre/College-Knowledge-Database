#algo

# Définition
On définit le tri fusion de la façon suivante: #!

Le tri fusion consiste à comparer deux éléments entre deux listes et de concaténer l'élément le plus petit dans la liste finale et d'avancer d'un indice sur la liste qui a été concaténée.
Une fois que l'indice dépasse la taille d'une des listes fournies, il s'arrête, et concatène le reste des éléments à la fin.
<!--ID: 1715690724124-->


## Implémentation
Voici une version de l'algorithme exprimé récursivement (on considère donc le première élément de la liste à chaque fois, et on se décale de 1 une fois concaténé.)
```python
def fusion(L1,L2):
	if (L1 == []):
		return L2
	if (L2 == []):
		return L1
	if (L1[0]<= L2[0]):
		R=fusion(L1[1: ], L2)
		R.insert(0, L1[0])
		return R
	R=fusion(L1, L2[1: ])
	R.insert(0, L2[0])
	return R
```

## Gestion de la monotonie
Il est possible de rendre le tri fusion optimal: #!
Pour rendre l'exécution optimale, on peut observer la monotonie d'une liste. Vérifier donc si une partie de la liste et trier et agir en conséquence.
<!--ID: 1715690724126-->


```python
def eclatement ( L, L1, L2) :
	listeL1 = True
	pred = L[0]
	L1.append(pred)
	i = 1
	while (i<len(L)):
		if (pred > L[i]):
			listeL1=not listeL1
		if listeL1:
			L1.append(L[i])
		else:
			L2.append(L[i])
		pred=L[i]
		i = i+1
```

```python
def triFusionMonotonies(L):
	if len(L)>1:
		L1 = []
		L2 = []
		eclatement(L,L1,L2)
		while (len(L2)>0):
			L=fusion(L1,L2)
			L1 = []
			L2 = []
			eclatement(L, L1, L2)
		return L1
	return L
```