Les matrices sont des [[Structure de données]] abstraites qui peuvent être à une ou à 2 dimensions.

Les matrices à une dimension sont équivalentes aux listes dans le langages C.

Les matrices à 2 dimensions peuvent être codée comme des tableaux à 2 dimensions. En C il s'agira donc d'un tableau de pointeurs, et donc d'un pointeur de pointeur:

```c
// Matrice 2x3
int** mat = (int*) malloc(2*sizeof(int*));
for(int i = 0; i<2; i++) {
	mat[i] = (int*) malloc(3*sizeof(int));
}
```

**Remarque:** Il est aussi courant en C, d'"aplatir" la matrice, et donc de dresser un tableau ayant les couples d'éléments `(i,j)` triés.
Pour accéder à la case `(i,j)`, on accèdera alors à l'index `i*n+j`