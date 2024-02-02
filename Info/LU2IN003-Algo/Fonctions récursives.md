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

Lors d'un appel récursif, on utilise une [[Piles]] pour gérer le [[Contexte d'une fonction]]