## Définition
Un [[Arbres binaires]] est dit parfait lorsque: #!

Tous ses niveaux sont remplis à part le dernier qui peut être rempli le plus à gauche

## Hauteur
La hauteur d'un arbre parfait de taille $n$ est de l'ordre de $$\Theta(\log(n))$$

## Représentation
On peut représenter un arbre parfait de la façon suivante:

L'arbre parfait peut être représenter sous forme de tableau. Le premier élément de ce tableau donne le nombre de nœuds contenu dans l'arbre. Le reste des éléments décrivent l'arbre niveau par niveau

*Exemple*: Le tableau `[10, 8, 5, 1, 6, 2, 4, 7, 3, 18, 9]` représente l'arbre![[Pasted image 20240514140250.png]]

### Accès
En représentant un arbre parfait avec un tableau $T$, on peut accéder à ses éléments de la façon suivante: #!

- $T[1]$ est la racine de l'arbre
- Si $2i \leq n$ alors $T[2i]$ est le fils gauche de $T[i]$
- Si $2i + 1 \leq n$ alors $T[2i + 1]$ est le fils droit de $T[i]$
- Si $i > 1$ alors $T\left[\lfloor \frac{i}{2} \rfloor\right]$ est le père de $T[i]$

### Insertion
Si un arbre parfait est représenté par un tableau $T$ l'insertion se fait de la façon suivante: #!

Si le tableau a une taille suffisante, on incrémente le nombre de nœud stocké en $T[0]$ de 1 et on ajoute le nouveau nœud à la dernière case non occupé du tableau 
