#struct 

## Définition
Un arbre binaire de recherche est un [[Arbre (Structure de données)|arbre binaire]] $A$ tel que: #!
$$\forall x \in A, \forall y \in A_g(x), \forall z \in A_d(x), y \leq x \leq z$$
<!--ID: 1715184202445-->


## Définition structurelle en étude
```c
typedef struct s_btree {
	int cle;
	struct s_btree* fd;
	struct s_btree* fg;
} btree;
```

## Propriété du parcours infixe
Pour un ABR, le parcours infixe de cet arbre nous donne: #!
Une liste triée de ses clés.
<!--ID: 1715184202446-->


## Recherche du plus petit et plus grand élément
Dans un ABR, le plus petit élément et le plus grand élément se trouvent respectivement: #!
Dans le nœuds le plus à gauche et dans le nœud le plus à droite de l'arbre
<!--ID: 1715184202448-->


### Algorithme de recherche en étude
En considérant la [[#Définition structurelle en étude]]
```c
int minABR(btree* abr) {
	if(!abr) return -1;

	if(!abr->fg) return abr->cle;
	return minABR(abr->fg);
} //O(h)


int maxABR(btree* abr) {
	if(!abr) return -1;

	if(!abr->fd) return abr->cle;
	return maxABR(abr->fd);
} // O(h)
```


## Problématique: Suppression
Supprimer un élément d'un ABR n'est pas trivial, car il est nécessaire que cette suppression ne perturbe pas la validité de sa structure.

### Suppression du maximum
On peut trouver un algorithme de suppression du maximum d'un ABR: #!
Observons déjà que le maximum d'un ABR, n'a pas de sous arbre droit. Ensuite, observons grâce à cela qu'il suffit de passer l'arbre gauche du maximum à droite
<!--ID: 1715184202449-->


#### Algorithme de suppression du maximum
On prends ici aussi le loisir de sauvegarder la valeur maximal de l'arbre dans un pointeur.
Cette fonction va renvoyer la nouvelle racine de l'arbre.
```c
btree* supprimeMaxABR(btree* abr, int* pmax) {

	if(!abr->fd) {
		// On a pas de sous arbre droit, c'est le maximum
		*pMax = abr->cle;
		btree* fg = abr->fg;
		free(abr);
		return fg; 
	}

	abr->fd = supprimeMaxABR(abr->fd, pmax);
	return abr;	

}
```

### Suppression d'un élément quelconque
On remarque par la suppression du maximum que l'idée est clair: on décale les sous arbres à gauche et à droite quand il n'y a pas de sous arbre gênant.

De manière général, lorsqu'on a deux sous arbre sur l'élément à supprimer dans ABR, alors #!
On cherche le plus grand élément du sous-arbre gauche (ou le plus petit élément du sous-arbre droit), on le met à la position de l'élément à supprimer, et on supprime l'élément dupliqué simplement (car il n'aura pas de fils droit (resp. fils fauche))
<!--ID: 1715184202451-->



#### Algorithme de suppression d'un élément
On choisit ici de procéder en cherchant le plus grand élément du sous-arbre gauche et de remplacer l'élément à supprimer par celui-ci.
```c
btree* supprimeABR(btree* abr, int val) {

	if(!abr) return;

	if(val < abr->cle) abr->fg = supprimeABR(abr->fg, val);
	else if(val > abr->cle) abr->fd = supprimeABR(abr->fd, val);

	else {
		if(!abr->fg) {
			// On décale ici sous-arbre droit à gauche
			btree* tmp = abr;
			abr = abr->fd;
			free(tmp);
		} else {
			abr->fg = supprimeMaxABR(abr->fg, abr->cle);
		}
	}
	return abr;

}
```


## Problématique: Equilibrage

## Annexes d'algorithme
### Validité structurelle d'un ABR
```c
int checkABR(btree* b) {
	if(!b) return 1;

	if(b->fg) {
		if(!checkABR(b->fg)) return 0;
		if(b->fg->cle >= b->cle) return 0;
	}
	
	if(b->fg) {
		if(!checkABR(b->fd)) return 0;
		if(b->fd->cle <= b->cle) return 0;
	}
	
	return 1;
}
```

### Recherche d'un élément dans un ABR
```c
btree* exists(btree* b, int val) {

	if(!b) return NULL;

	if(b->cle == val) return b;

	if(val > b->cle) return exists(b->fd, val);
	if(val < b->cle) return exists(b->fg, val);

} // O(h)
```

### Insertion d'un élément dans un ABR
On doit bien maintenir la structure de l'arbre.
`btree* creer(int val, btree* fg, btree* fd)` créer une nœud d'arbre ayant la valeur `val`, le fils gauche `fg` et le fils de droit `fd`
```c
btree* insererABR(btree* b, int val) {
	if(!b) return creer(val, NULL, NULL);

	if(b->cle > val) {
		if(!b->fg) b->fg = creer(val, NULL, NULL);
		else insererABR(b->fg, val)
	}

	if(b->cle > val) {
		if(!b->fd) b->fd = creer(val, NULL, NULL);
		else insererABR(b->fd, val)
	}
}
```