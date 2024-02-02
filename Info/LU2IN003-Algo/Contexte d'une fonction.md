#algo
Le contexte d'une fonction est une [[Piles|pile]] contenant l'ensemble des valeurs des paramètres et des variables des fonctions.

Lorsqu'une fonction à terminer de s'exécuter, son contexte est progressivement retiré de la pile de gestion:

# Exemple avec factorielle
```python
def factorielle(n):
	print("Appel de factorielle avec n = ", n)
	int res
	if n==0:
		res = 1
	else:
		res = n*factorielle(n-1)
	print("Resultat pour n = ", res)
	return res

factorielle(4)
```

## Etat de la pile
A l'arrivé dans le cas d'arrêt, la pile a cet état
```
res = 1 * ...
n = 0
res = 1 *
n = 1
res = 2 * ...
n = 2
res = 3 * ...
n = 3
res = 4 * ...
n = 4
```
Pour commencer à afficher les résultats, la pile va progressivement être dépilée

*Output*

```
Appel de factorielle avec n = 4
Appel de factorielle avec n = 3
Appel de factorielle avec n = 2
Appel de factorielle avec n = 1
Appel de factorielle avec n = 0
Resultat pour n = 0, 1
Resultat pour n = 1, 1
Resultat pour n = 2, 2
Resultat pour n = 3, 6
Resultat pour n = 4, 24
```
On observe bien l'empilement et le dépilement de la pile.
## Preuve de la terminaison et de la validité

Par récurrence sur $n \in \mathbb{N}$, on note $\Pi(n)$: "`factorielle(n)` se termine et renvoie $n!$"

Initialisation:
Si $n=0$ il n'y a pas d'appelle récursif. Le programme renvoie $1$ et $0! = 1$ donc $\Pi(0)$ est vraie

Hérédité
Montrons que $\forall n \in \mathbb{N}, \Pi(n) \Rightarrow \Pi(n+1)$

On a que `factorielle(n+1)` appelle `factorielle(n)` qui termine par la propriété $\Pi(n)$.
Les autres opérations sont élémentaires. Ainsi donc `factorielle(n+1)` se termine.

On a de plus:
`res = (n+1)*factorielle(n)` qui par $\Pi(n)$ nous donne `res = (n+1) * n! = (n+1)!`

Donc finalement $\Pi(n+1)$ est vraie

$\forall n \in \mathbb{N}$, on note $\Pi(n)$: "`factorielle(n)` se termine et renvoie $n!$"
$$\tag*{$\blacksquare$}$$
