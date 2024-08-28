#algo
## Définition
La complexité d'un algorithme est #!
Une évaluation du nombre d'instruction élémentaire lors de l'exécution de l'algorithme.
Il ne s'agit pas de faire un comptage précis selon les paramètres, mais de faire une approximation avec les [[La notation de Landau]].
<!--ID: 1715690724099-->


## Complexité pire et meilleur cas
L'évaluation de la complexité dépend du paramètre fourni à l'algorithme. 
On peut évaluer la complexité dans le pire des cas, donc la borne supérieur (c'est en général celle qu'on utilise pour étudie un algorithme).
Mais il est aussi possible d'évaluer le meilleur cas.

*Exemple*: Lorsqu'on recherche un élément dans le tableau...
- Le meilleur des cas est $\Omega(1)$, l'élément est à la première cas du tableau.
- Le pire des cas est $O(n)$, l'élément n'est pas dans le tableau.

**ATTENTION**: La complexité est asymptotique, lorsque l'on étudie, c'est lorsque $n$ est grand. Il est absurde de justifier une complexité en fonction de la taille de $n$

## Exemple d'évaluation

On se propose d'étudier une fonction calculant la somme des $n$ premiers entiers
### L'exemple basique: somme
#### Itératif
On considère l'algorithme $\mathcal{A}$ calculant la somme:
```python
def somIte(n):
	res = 0
	for i in range(1, n + 1):
		res = res + i
	return res
```

On pose $c_i$ le nombre d'instruction à la $i^{ème}$ itération.
Ici $\forall i, c_i = 1$ donc le nombre total d'instruction pour un paramètre $n$ est de:
$$ \sum_{i=1}^{n+1}c_i = n $$
La complexité est de $\Theta(n)$
#### Récursif
On considère l'algorithme $\mathcal{A}$ calculant la somme:
```python
def somRec(n):
	if n == 0:
		return 0
	else:
		return n + somRec(n-1)
```

Pour évaluer la complexité d'une fonction récursive ==il faut évaluer la suite récurrente==.

Soit $u_n$ le nombre d'opérations effectuée par l'appelle `somRec(n)`.
Il y a 2 opérations élémentaires: 1 test avec le `if else`, 1 `return` 

Alors $u_n$ est la suite récurrente définie par: $u_n = 2 + u_{n-1}$

Par substitutions observons que:
$u_n  = u_{n-1} + 2 = u_{n-2} +4 = u_0 + 2n = 2n+1$
Sa complexité est donc aussi de $\Theta(n)$

### Exemple complexe: Fibonacci

#### Itératif
```python
def fibo_it(n):
	if(n == 0) or (n==1):
		return n
	x = 0; y = 1;
	for i in range(2, n+1):
		z = x + y; x = y; y = z;
	return y 
```

Soit $c_i$ le nombre d'addition effectué à la $i^{ème}$ itération. On alors:
$$\sum_{i=2}^{n+1}c_i = n $$
La complexité est alors de $\Theta(n)$
#### Récursif
```python
def fibRec(n):
	if(n==0) or (n==1):
		return n
	else:
		return fibRec(n-1) + fibRec(n-2)
```

Soit $u_n$ le nombre d'additions effectués par l'appel de `fibRec(n)`. (Compter le nombre d'addition par rapport aux opérations élémentaires, n'est pas important, le résultat sera le même)

On a $u_n = u_{n-1} + u_{n-2} + 1$ si $n>1$ et $u_0 = u_1 = 0$

Remarquons que $u_n = F_{n+1} - 1$
Or on sait que $F_n \geq \frac{1}{\sqrt{5}}(\rho^n-1)$ où $\rho = \frac{1 + \sqrt{5}}{2}$ le nombre d'or

La complexité de cet algorithme est alors $\Omega(\rho^n)$. Comme $\rho > 1$ la complexité est exponentielle