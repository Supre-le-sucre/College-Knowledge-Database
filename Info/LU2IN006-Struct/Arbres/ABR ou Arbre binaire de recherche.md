#struct 

## Définition
Un arbre binaire de recherche est un [[Arbre (Structure de données)|arbre binaire]] $A$ tel que: #!
$$\forall x \in A, \forall y \in A_g(x), \forall z \in A_d(x), y \leq x \leq z$$

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

## Recherche du plus petit et plus grand élément
Dans un ABR, le plus petit élément et le plus grand élément se trouvent respectivement: #!
Dans le nœuds le plus à gauche et dans le nœud le plus à droite de l'arbre

### Algorithme de recherche en étude
En considérant la [[#Définition structurelle en étude]]
```c
int minABR(btree* abr) {
	if(!abr) return -1;

	if(!abr->fg) return abr->cle;
	return minABR(abr->fg);
}


int maxABR(btree* abr) {
	if(!abr) return -1;

	if(!abr->fd) return abr->cle;
	return minABR(abr->fd);
}
```