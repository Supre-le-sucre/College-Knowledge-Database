Un algorithme $\mathcal{A}$ qui résout un problème $P$ est une [[Programme]] qui vérifie les deux propriétés suivantes:

- Terminaison: Pour tout instances du [[Problème]], l'algorithme se termine
- Validité: Pour tout instances du [[Problème]], l'algorithme renvoie la valeur attendue

## Exemple itératif Fibonacci

On pose le [[Programme]] $\mathcal{P}$ calculant le terme $n$ de la suite de Fibonacci.
```python
def fibo_it(n):
	if(n == 0):
		return 0
	x = 0; y = 1; i = 1
	while(i<n):
		z = x + y; x = y
		y = z; i = i + 1
	return y 
```

Ce programme satisfait-t-il la définition d'un algorithme $\mathcal{A}$

### Terminaison
La boucle est susceptible d'empêcher la terminaison, il faut donc prouver que ce n'est pas le cas.

Le corps de la boucle est composée d'opération élémentaire.
La boucle est exécuté $n-1$ fois.

Le programme se terminera alors $\forall n \in \mathbb{N}$

### Validité

Il faut étudier les variations de variables $x$ et $y$

- A l'initialisation, $x_1 = 0, y_1 =1$

On note, $\forall i \in \set{1, \cdots, n}$, $x_i$ et $y_i$, respectivement, la valeur de $x$ et de $y$ à la fin du corps de la boucle pour la valeur $i$.

#### Identifier l'invariant


