## Définition de la rotation
Une rotation est une méthode d'équilibrage. Son fonctionnement et ses propriétés principales sont les suivantes: #!

- Une rotation conserve le parcours infixe de l'arbre, ce qui permet notamment d'équilibrer les ABR
- Une rotation sur un [[Arbres AVL]] ne conserve pas ses propriétés
- Une rotation peut avoir lieu à droite ou à gauche telle que: ![[Pasted image 20240508174027.png]]
<!--ID: 1715184202435-->


## Double rotation
Une double rotation est définie comme: #!
Deux rotations classique, la première à gauche sur le sous-arbre gauche, la seconde à droite sur l'arbre courant ![[Pasted image 20240508174425.png]]
<!--ID: 1715184202439-->



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

## Algorithme d'équilibrage
On peut donner un algorithme d'équilibrage suivant, à chaque insertion ou suppression d'un élément dans un [[Arbres AVL]]: #!

Depuis la racine jusqu'à l'élément à supprimer ou insérer, on vérifie pour 
- $A$ un arbre 
- $G, D$ les sous-arbres gauche et droit
- $g,d$ les sous-arbres gauche et droit de $G$
```
Si H(G) - H(D) = 2 
	Si H(g) < H(d) Alors rotation à gauche de G
	Rotation à droite de A
Si H(G) - H(D) = -2
	Si H(g) < H(d) Alors rotation à droite de D
	Rotation à gauche de A
```
<!--ID: 1715184247852-->

