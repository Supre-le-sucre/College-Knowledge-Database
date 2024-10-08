## Définition
On définit une Skip List de la façon suivante: #!

Une skip list (ou liste à enjambement/liste à saut) est une structure de donnée ==probabiliste== constituée de plusieurs couche appelé "niveau" (noté $L_0, L_1, \dots$) correspondant à une liste chaînée particulière.
La couche $L_0$ (ou première couche) correspond à la liste ==triée== que l'on souhaite stocker. Les autres couches représentent des "raccourcis" que l'on construit de façon itérative de la façon suivante:
Pour un élément $e$ de la couche $L_i$ celui-ci a une probabilité $p$ de faire partie de la couche $L_{i+1}$, et si c'est le cas, l'élément $e$ de $L_{i+1}$ doit faire référence à l'élément $e$ de $L_i$ ![[Pasted image 20240509171149.png]]
<!--ID: 1715272259446-->


## Implémentation
On considère l'implémentation suivante:
Comme on ne connaît pas à l'avance le nombre de couche, elles sont stockées dans une liste doublement chaînée
```c
typedef struct s_cell {
	int val;
	struct s_cell* next;
	struct s_cell* below;
} Cell;

typedef struct s_layer {
	int level;
	Cell* first;
	struct s_layer* above;
	struct s_layer* below;
} Layer;

typedef struct {
	float p;
	Layer* top;
	Layer* bottom;
} SkipList;
```

## Recherche dans une skip list
L'opération de recherche se déroule de la manière suivante: #!

Pour un élément $v$ recherché, on commence d'abord la recherche sur la plus haute couche. On parcourt la liste jusqu'à trouver $e$, un élément ==inférieur ou égal== à $v$ et dont l'élément suivant n'==existe pas== ou est ==strictement supérieur== à $v$. Dans ce cas, on passe à la couche d'en dessous en utilisant la référence de $e$, et on poursuit la recherche. Si la première couche est atteinte, la recherche a le même comportement qu'une liste chaînée classique ![[Pasted image 20240509171553.png]]
<!--ID: 1715272259451-->


### Algorithme implémenté
On considère alors l'implémentation suivante:
```c
int skiplist_search(SkipList* sl, int val) {

	// On cherche la première couche compatible avec la recherche
	Layer* currLayer = sl->top;
	while(currLayer && currLayer->first->val > val) {
		currLayer = currLayer->below;
		
	}
	if(!currLayer) return 0;

	Cell* currCell = currLayer->first;
	while(currCell && currCell->val != val) {
		if(!currCell->next || currCell->next->val > val) {
			currCell = currCell->below;
		}
		else {
			currCell = currCell->next;
		}
	}

	if(curCell) return 1;
	return 0;

}
```

## Suppression d'un élément dans une skip list
La suppression se déroule de la façon suivante: #!

On cherche l'élément à partir de la couche la plus haute, et dès qu'on trouve cet élément, on le supprime des couches supérieurs.
Il n'est pas nécessaire de vérifier autre chose, la liste restera trié et la probabilité d'existence des éléments ne sera pas altérée
<!--ID: 1715272259454-->


### Implémentation de l'algorithme de suppression
On implémente donc l'algorithme suivant: 

```c
void skiplist_delete(SkipList* sl, int val) {

	// Recherche de la première couche compatible
	Layer* currLayer = sl->top
	while(currLayer && currLayer->first->val > val) {
		currLayer = currLayer->below;
	}

	if(!currLayer) return;

	Cell* currCell = currLayer->first;
	// On travaille d'abord avec les cellules en début de couche
	while(currCell && currCell->val == val) {
		if(!currCell->suiv) {
			// Le layer courant doit être supprimé 
			// car l'élément à supprimer est l'unique élément
			
			// Si la couche courante est la couche la plus haute
			// Alors le "top" va changer:
			if(currLayer == sl->top) {
				sl->top = currLayer->below;
			}
			Layer* tmp = currLayer->below;
			free(currLayer)
			currLayer = tmp;
		}
		else {
			currLayer->first = currCell->suiv;
			currLayer = currLayer->below;
		}
		free(currCell);	
		// Comme on ne bouge pas dans les indices ici
		// On ne bouge que dans les couches.
		if(currLayer) currCell = layer->first;
		else currCell = NULL;
	}

	// Si des cellules en tête de liste devait être supprimée
	// C'est maintenant chose faite.

	while(currCell) {
		if(!currCell->next || currCell->next->val > val) {
			// Plus de cellule à supprimer dans ce layer
			currCell = currCell->below;
		}
		else {
			if(currCell->next->val == val) {
				Cell* toFree = currCell->next;
				currCell->next = currCell->next->next;
				free(toFree);
				// On ne bouge pas, les éléments suivants
				// sont à réévaluer
			}
			else {
				currCell = currCell->suiv;
			}
		}
	}
}
```

## Insertion d'un élément dans une skip list
L'algorithme d'insertion procède comme suit: #!

on cherche d'abord où insérer l'élément dans la première couche, donc on procède comme dans la fonction de recherche: On part de la couche la plus haute, et on descend qui suit l'élément courant est strictement plus grand que l'élément à insérer.
Une fois sur la première couche, on insère l'élément comme dans une liste chaînée classique. On ajoute ensuite l'élément à la couche d'au dessus avec une probabilité $p$ et on continue en ajoutant des couches si nécessaire
<!--ID: 1715272259457-->


## Remarque sur $p$
On observe les choses suivantes en fonction de $p$ pour une skip list: #!

Si $p$ vaut 0, une skip list est une simple liste chaînée, plus il est proche de $1$ plus il y aura de couche, donc plus de raccourcis mais aussi une plus grande mémoire.
La valeur de $p$ permet définir le compromis entre temps de calcul et espace mémoire utilisé.
<!--ID: 1715272259459-->


## Complexité
Pour une structure de donnée probabiliste, il n'est pas possible d'établir une complexité exacte. On parle alors de complexité en espérance. Pour une skip list on observe les complexité en espérance spatiale et temporelle suivante, pour une probabilité de $p=\frac{1}{2}$: #!

- Une complexité spatiale en $O(n)$
	En effet, la probabilité qu'un élément fasse partie de la couche $L_i$ est de $\left(\frac{1}{2}\right)^i$ donc en moyenne on a un nombre de cellule total de... $$n(1+\frac{1}{2}+\frac{1}{4}+\frac{1}{8}+\dots) = 2n$$
- Une complexité temporelle de $O(\log_2(n))$
	Dans une skip list cette complexité temporelle est la même pour l'insertion, la suppression et la recherche. En effet la hauteur moyenne d'une skip list de probabilité $p$ est en $\log_p(n)$ 
<!--ID: 1715272259462-->


Une skip list est une alternative aux [[Arbres AVL]]