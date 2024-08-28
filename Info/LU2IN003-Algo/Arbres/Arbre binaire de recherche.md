## Définition
On définit inductivement l'ensemble des [[Arbres binaires]] de recherche $ABR$ de la façon suivante: #!

- $\emptyset \in ABR$ 
- $(x, G, D) \in ABR$ si $G, D \in ABR$, toutes les clés de $G$ sont inférieures à $x$ et toutes les clefs de $D$ sont supérieures à $x$
<!--ID: 1715690724136-->


## Propriété caractéristique
On observe qu'un arbre binaire a une propriété propre: #!

Les parcours infixe d'un $ABR$ donne toujours une liste rangée dans l'ordre croissant
<!--ID: 1715690724137-->


## Recherche
La recherche dans un ABR est efficace: #!
Il suffit de comparer la clé avec l'élément recherché pour vérifier si l'on doit évaluer le sous-arbre gauche ou le sous-arbre droit.
La complexité est en $O(h)$ où $h$ la hauteur de l'arbre
<!--ID: 1715690724139-->



## Insertion
L'insertion dans un ABR est simple: #!

Lorsque l'on insère une nouvelle clé, on vérifie si celle-ci est plus grande ou plus petite que la clé courante,
- dans le premier cas, on continue à droite
- dans l'autre on continue à gauche
L'insertion se fait dans une feuille
La complexité est en $O(h)$ où $h$ la hauteur de l'arbre
<!--ID: 1715690724141-->


## Recherche de maximum et de minimum
Ces recherches sont également efficace dans un ABR: #!

Le maximum est toujours le nœud le plus à droite, le minimum est toujours le nœud le plus à gauche.
La complexité dépend donc de la hauteur de la branche droite ou gauche
<!--ID: 1715690724142-->


## Suppression du maximum
Pour supprimer le maximum dans un ABR: #!

On remplace le nœud le plus à droite par son fils le plus à gauche, et on supprime le fils le plus à gauche
<!--ID: 1715690724144-->


## Suppression de la racine
Pour supprimer la racine dans un ABR: #!

Si le sous-arbre gauche est vide, il suffit de remplacer cette racine par le sous-arbre droit.
Sinon, il faut remplacer la racine par le maximum du sous-arbre gauche (donc l'élément le plus à droite du sous-arbre gauche) et on déplace ensuite les éléments convenablement.
<!--ID: 1715690724146-->



## Suppression d'un élément quelconque dans un ABR
Pour supprimer un élément quelconque dans ABR: #!

On cherche à se ramener à la [[#Suppression de la racine]]
Ainsi donc, si l'élément en cours est l'élément à supprimer on se comporte comme tel. Sinon on cherche l'élément dans l'ABR et on supprime en conséquence. D'où l'algorithme suivant:
```python
def supp(x, T):
	if estABvide(T):
		return T
	if x == T.clef:
		return ABRmoinsRacine(T)
	if x < T.clef:
		return AB(T.clef, supp(x, T.gauche), T.droit)
	return AB(T.clef, T.gauche, supp(x, T.droit))
```
<!--ID: 1715690724147-->
