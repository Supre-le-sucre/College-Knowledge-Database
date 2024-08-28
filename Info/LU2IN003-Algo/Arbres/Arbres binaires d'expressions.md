## Définition
On définit inductivement l'ensemble des [[Arbres binaires]] d'expressions $ABE$ tel que: #!

- $(x, \emptyset, \emptyset) \in ABE$ où $x$ est une valeur numérique
- $(x, G, D) \in ABE$ où $x$ est un opérateur $+,-,\times,/$ et $G, D \in ABE$
<!--ID: 1715690724161-->


*Exemple*:
![[Pasted image 20240514134315.png]]

## Propriétés
On observe dans un arbre binaire d'expressions les propriétés suivantes: #!

- Chaque nœud interne a exactement 2 fils
- Chaque nœud internes est un opérateur
- Chaque feuille est une valeur numérique
- Le nombre de valeurs numériques est égale aux nombres d'opérateurs incrémenté de 1
<!--ID: 1715690724163-->


## Evaluation
On évalue un arbre binaires d'expressions par l'algorithme suivant: #!

```python
def eval(T):
	if estABfeuille(T):
		return T.clef
	if T.clef == "+":
		return eval(T.gauche) + eval(T.droit)
	if T.clef == "-":
		return eval(T.gauche) - eval(T.droit)
	if T.clef == "*":
		return eval(T.gauche) * eval(T.droit)
	if T.clef == "/":
		return eval(T.gauche) / eval(T.droit)
```
La complexité de l'évaluation est en $\Theta(n)$
<!--ID: 1715690724165-->


## [[Arbres binaires#Parcours d'arbre binaire|Parcours]] d'un arbre binaire d'expression

Pour un arbre binaire d'expression on observe que les différents parcours donne un moyen d'évaluation différents

- Préfixe: les opérandes sont avant les éléments à évaluer
	Dans la liste donnant le parcours préfixe, un opérande peut être suivi:
	- D'un opérande (dans ce cas on a un calcul à faire avant)
	- De deux nombres (dans ce cas on évalue le résultats: gauche. opérande. droite)
	Le parcours préfixe commence toujours par un opérande
- Infixe:
	Dans la liste donnant le parcours infixe, l'expression arithmétique est exprimé dans le langage naturel (mais attention, les priorités de calcul ne sont pas correctement exprimées)
 - Suffixe: les opérandes sont après les éléments à évaluer