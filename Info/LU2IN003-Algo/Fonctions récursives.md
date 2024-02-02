#algo 

Une fonction récursive est une fonction qui s'appelle elle-même en son corps:

*Exemple*
```python
def factorielle(n):
	if n==0:
		return 1
	else:
		return n*factorielle(n-1)
```

Lors d'un appel récursif, on utilise une [[Piles]], qui permet de gérer le dernier élément arrivé en premier (et donc la fonction qui gère le cas d'arrêt de la fonction récursive) 