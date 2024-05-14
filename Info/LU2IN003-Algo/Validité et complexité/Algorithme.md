#algo
Un algorithme $\mathcal{A}$ qui résout un problème $P$ est un [[Programme]] qui vérifie les deux propriétés suivantes: #!

- Terminaison: Pour tout instances du [[Problème]], l'algorithme se termine
- Validité: Pour tout instances du [[Problème]], l'algorithme renvoie la valeur attendue
<!--ID: 1715690724101-->


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

Ce programme satisfait-t-il la définition d'un algorithme $\mathcal{A}$ ?

### Terminaison
La boucle est susceptible d'empêcher la terminaison, il faut donc prouver que ce n'est pas le cas.

Le corps de la boucle est composée d'opérations élémentaires.
La boucle est exécuté $n-1$ fois.

Le programme se terminera alors $\forall n \in \mathbb{N}$

### Validité

Il faut étudier les variations de variables $x$ et $y$

- A l'initialisation, $x_1 = 0, y_1 =1$

On note, $\forall i \in \set{1, \cdots, n}$, $x_i$ et $y_i$, respectivement, la valeur de $x$ et de $y$ à la fin du corps de la boucle pour la valeur $i$.

#### Identifier l'invariant

Pour plus de visibilité, dressons le tableau d'exécution pour $n =6$ 

| i | 1 | 2 | 3 | 4 | 5 | 6 |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| $x_i$ | 0 | 1 | 1 | 2 | 3 | 5 |
| $y_i$ | 1 | 1 | 2 | 3 | 5 | 8 |
On sait aussi que les valeurs de Fibonacci sont les suivantes:
$(F_n)_{n \in \mathbb{N}} = (0, 1, 1, 2, 3, 5, 8, \cdots)$


Les valeurs de $y_i$ semble prendre la forme de la valeur de $F_i$. Tentons alors de montrer que $y_i = F_i$
Dans ce cas, puisque l'algorithme se termine lorsque $i = n$, et renvoie $y_n =F_n$, si notre égalité est vérifiée, le programme $\mathcal{P}$ est valide.

On utilise ici le [[Raisonnement par récurrence]] pour prouver notre égalité.

Soit $\Pi(i) : y_i = F_i$

- Initialisation (ce qu'il se passe avant la boucle) $i=1, y_i = y_1 = 1= F_1$ donc $\Pi(1)$ est vraie
- Hérédité, montrons $\Pi(i) \Rightarrow \Pi(i+1)$
	On sait que $y_i$ = $F_i$ mais on est bloqué. car $z_i = x_i + y_i$ et nous n'avons aucune information sur $x$


#### Prouver la validité
Reposons alors la propriété, cette fois-ci, en prenant compte de $x$

Soit $\Pi(i) : y_i = F_i$ et $x_i = F_{i-1}$
- Initialisation (ce qu'il se passe avant la boucle) $i=1, y_i = y_1 = 1= F_1$ et $x_0 = 0 =F_0$ donc $\Pi(1)$ est vraie
- Hérédité, montrons $\Pi(i) \Rightarrow \Pi(i+1)$
	On sait que $y_i$ = $F_i$ et $x_i = F_{i+1}$
	$z_i =x_i + y_i = F_{i-1}+F_i = F_{i+1}$
	D'où...
	$x_{i+1} = y_i = F_i$
	$y_{i+1} = z_i = F_{i+1}$
	Donc $\Pi(i+1) est vraie

En conclusion, $\forall i \leq n, x_i = F_{i-1}$ et $y_i = F_i$
Pour $i=n$, $y_n = F_n$, et le programme renvoie $y_n$
Le programme est valide.

Finalement le programme $\mathcal{P}$ est bien un algorithme $\mathcal{A}$ permettant de calculer la suite de Fibonacci


## Exemple minimum dans un tableau

On pose le problème $P$ suivant:
`tab[0 ... n-1]` est un tableau de $n$ entiers
`recherche_min(tab, d, f)` retourne l'indice d'un élément du tableau `tab[d ... f]` de valeur minimum pour $0 \leq d \leq f <n$

On propose alors le programme $\mathcal{P}$ suivant
```python
def recherche_min(tab, d, f):
	imin = d; i=d+1
	while i <= f:
		if tab[i]<tab[imin]:
			imin = i
		i=i+1
	return imin
```

### Terminaison

Le corps de la boucle n'est composé que d'opérations élémentaires, et la boucle s'exécute $f-d$ fois, donc le programme $\mathcal{P}$ s'arrête $\forall f, d$
### Validité pour une instance particulière
On considère l'instance $I$ du problème $P$ pour $tab=[6, 3, 1, 7, 5], d=1, f=4$
le plus petit élément entre les indices 1 et 4 est 1, son indice est 2 donc:
`recherche_min(tab, d, f) = 2`

Vérifions si notre programme est valide pour $I$.
On dresse le tableau des variables pour une telle exécution

| i      | 1 | 2 | 3 | 4 | 5 |
|--------|---|---|---|---|---|
| $i_{min_i}$ | 0 | 1 | 2 | 2 | 2 |
Le programme est valide pour l'instance $I$

### Identification de l'invariant

Remarquons que $\forall i \in [d+1, f+1]$, $i_{min_i}$ est l'indice du plus petit élément entre les indices $d$ et $i-1$ (i.e. $\forall k \in [d, i-1], tab[k] \geq tab[i_{min_i}]$)

### Preuve de la validité

On prouvera la validité par [[Raisonnement par récurrence]] sur $i \in [d+1, f+1]$
On pose $\Pi(i) = \forall k \in [d, i-1], tab[k] \geq tab[i_{min_i}]$

- Initialisation
	$i=d+1$ et $i_{min_i}=i_{min_{d+1}} = d$
	On a que $k \in [d, i-1]$ donc $k = d$
	Soit alors $tab[k] = tab[d] \geq tab[i_{min_{d+1}}]$ 

- Hérédité
	Soit $i \in [d+1, f]$ tel que $\Pi(i)$ est vraie
	- 1er cas $tab[i] < tab[i_{min_i}]$
		Dans ce cas $i_{min_{i+1}}$
		Par $\Pi(i)$, on a que $\forall k \in [d, i-1], tab[k] \geq tab[i_{min_i}]$
		Et $tab[i_{min_i}] > tab[i] = tab[i_{min_{i+1}}]$
		Donc finalement $\forall k \in [d, i]$, $tab[k] \geq tab[i_{min_{i+1}}]$

	- 2e cas $tab[i] \geq tab[i_{min_i}]$
		$i_{min_{i+1}} = i_{min_i}$
		Par $\Pi(i)$, on a que $\forall k \in [d, i-1], tab[k] \geq tab[i_{min_i}] = tab[i_{min_{i+1}}]$
		Puisque $tab[i] \geq tab[i_{min_i}] = tab[i_{min_{i+1}}]$ 
		On a bien que $\forall k \in [d, i]$, $tab[k] \geq tab[i_{min_{i+1}}]$

Ainsi donc le programme $\mathcal{P}$ est bien un algorithme $\mathcal{A}$ répondant au problème $P$
