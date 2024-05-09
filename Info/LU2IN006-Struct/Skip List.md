## Définition
On définit une Skip List de la façon suivante: #!

Une skip list (ou liste à enjambement/liste à saut) est une structure de donnée ==probabiliste== constituée de plusieurs couche appelé "niveau" (noté $L_0, L_1, \dots$) correspondant à une liste chaînée particulière.
La couche $L_0$ (ou première couche) correspond à la liste ==triée== que l'on souhaite stocker. Les autres couches représentent des "raccourcis" que l'on construit de façon itérative de la façon suivante:
Pour un élément $e$ de la couche $L_i$ celui-ci a une probabilité $p$ de faire partie de la couche $L_{i+1}$, et si c'est le cas, l'élément $e$ de $L_{i+1}$ doit faire référence à l'élément $e$ de $L_i$ ![[Pasted image 20240509171149.png]]

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

### Implémentation de l'algorithme de suppression
On implémente donc l'algorithme suivant: 

```c
Cell* skiplist_delete(SkipList* sl, int val) {

	// Recherche de la première couche compatible
	Layer* currLayer = sl->top
	while(currLayer && currLayer->first->val > val) {
		currLayer = currLayer->below;
	}

	if(!currLayer) return NULL;

	Cell* currCell = currLayer->first;
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
		currCell = currLayer->first
	}

}
```