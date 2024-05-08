#struct 

## Définition 
Un arbre AVL ou un arbre d'Adel'son-Vel'skii et Landiis peut se définir de la façon suivante: #!

Un arbre AVL vérifie la propriété que la différences des hauteurs du fils gauche et du fils droit ne peut excéder 1
**Remarque**: On peut donc en déduire que la hauteur d'un arbre AVL de $n$ nœuds est de l'ordre de $\log_2(n)$

## Implémentation en C

### Définition  structurelle
On peut définir un AVL comme la structure suivante:
```c
typedef struct s_avltree {
	int cle;
	int hauteur; // Hauteur de l'arbre courant

	struct s_avltree* fd;
	struct s_avltree* fg;
	
} AVL;
```

### Création d'un nouveau nœud
De fait on créer un nouveau nœud de la façon suivante:
```c
AVL* cree(int val, AVL* fg, AVL* fd) {
	AVL* n = (AVL*) malloc(sizeof(AVL));
	n->cle = val;
	n->fg = fg;
	n->fd = fd;

	// On met à jour la hauteur du noeud courant
	n->hauteur = 1 + max(
		(fg) ? -1 : fg->hauteur,
		(fd) ? -1 : fd->hauteur
	);

	return n;
}
```
