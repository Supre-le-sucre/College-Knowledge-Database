## Définition de la rotation
Une rotation est une méthode d'équilibrage. Son fonctionnement et ses propriétés principales sont les suivantes: #!

- Une rotation conserve le parcours infixe de l'arbre, ce qui permet notamment d'équilibrer les ABR
- Une rotation sur un [[Arbres AVL]] ne conserve pas ses propriétés
- Une rotation peut avoir lieu à droite ou à gauche telle que: ![[Pasted image 20240508174027.png]]

## Double rotation
Une double rotation est définie comme: #!
Deux rotations classique, la première à gauche sur le sous-arbre gauche, la seconde à droite sur l'arbre courant ![[Pasted image 20240508174425.png]]


## Implémentation des rotations
Les rotations ont une complexité de $\Theta(1)$ 
En considérant la structure [[Arbres AVL#Définition structurelle|d'arbre AVL]] on a donc

```c
AVL* rotDroite(AVL* rac) {
	AVL* nvrac = rac->fg;

	rac->fg = nvrac->fd;
	nvrac->fd = rac;

	majHauteur(rac);
	majHauteur(nvrac);
	
	return nvrac;
}

AVL* rotGauche(AVL* rac) {
	AVL* nvrac = rac->fd;

	rac->fd = nvrac->fg;
	nvrac->fg = rac;

	majHauteur(rac);
	majHauteur(nvrac);

	return nvrac;
}

AVL* doubleRotDroite(AVL* rac) {
	rac->fg = rotGauche(rac->fg);
	majHauteur(rac);
	return rotDroite(rac);
}
```