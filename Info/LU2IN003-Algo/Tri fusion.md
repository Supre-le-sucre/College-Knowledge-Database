Le tri fusion consiste à comparer deux éléments entre deux listes et de concaténer l'élément le plus petit dans la liste finale et d'avancer d'un indice sur la liste qui a été concaténée.

Une fois que l'indice dépasse la taille d'une des listes fournies, il s'arrête, et concatène le reste des éléments à la fin.

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