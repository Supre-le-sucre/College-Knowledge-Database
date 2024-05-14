#algo 

# Définition
On définit une fonction récursive comme: #!
une fonction qui s'appelle elle-même en son corps:
<!--ID: 1715690724096-->


*Exemple*
```python
def factorielle(n):
	if n==0:
		return 1
	else:
		return n*factorielle(n-1)
```

Lors d'un appel récursif, on utilise une [[Piles|pile]] pour gérer le [[Contexte d'une fonction]]