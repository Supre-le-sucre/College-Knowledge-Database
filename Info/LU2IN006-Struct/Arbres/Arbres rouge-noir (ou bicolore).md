Un arbre rouge noir est une variante aux [[Arbres AVL]] nécessitant moins de rotations en pratique

## Définition
Un arbre rouge-noir (ou bicolore) est un arbre respectant les propriétés suivantes: #!

- Il s'agit d'un [[ABR ou Arbre binaire de recherche]]
- Chaque nœud est de couleur noire ou rouge
- la racine est toujours de couleurs noire
- les fils d'un nœud rouge sont toujours de couleur noire
- si un nœud a moins de deux fils, on lui ajoute un nœud fictif noir
- le nombre de nœuds noirs sur un chemin de la racine vers une feuille est toujours le même et on l'appelle "hauteur noire"

## Observation sur la longueur d'un chemin
Dans un arbre rouge-noir on peut observer que: #!
Le plus long chemin de la racine vers une feuille est au plus deux fois plus long que le plus petit chemin. De plus la haute $h$ est donc au plus égale à $2h_N$

### Preuve
Chaque chemin passe exactement, par définition, par $h_N$ nœuds noirs. Le plus petit chemin possède donc ==au moins== $h_N$ nœuds.
De plus par définition, il n'est pas possible sur un même chemin d'avoir 2 nœuds rouges consécutifs, donc le plus long chemin alterne les nœuds rouges et noirs et a donc une taille de $2h_N$

## Hauteur d'un arbre rouge-noir
On observe que: #!
La hauteur d'un arbre rouge noir est de l'ordre de $O(log(n))$

### Preuve
On montre ceci par récurrence.
$\Pi(n)$: "Un arbre rouge noir de de hauteur noire $h_N = n$ vérifie $n \geq 2^{h_N}-1$"

Pour $h_N = 0$ alors on a forcément que $n=0$ car la racine est forcément noire

Pour un arbre tel que $h_N = n$, observons que comme la racine est forcément noire, les sous-arbres gauche et droit ont forcément une hauteur noire diminuée de 1.
Par hypothèse de récurrence ces sous-arbres possède au moins $2^{h_N - 1} - 1$ nœuds

Soit $n \geq 1 + 2(2^{h_N - 1} - 1)$ car on ajoute la racine.
Mais donc dans ce cas on a bien $n \geq 2^{h_N} - 1$

On a alors $h_N \leq \log_2(n+1)$

## Implémentation C
On donne la définition structurelle suivante:

```c
#define NOIR 0
#define ROUGE 1

typedef struct arn {
	int val;
	int couleur;
	struct arn* fg;
	struct arn* fd;
	struct arn* pere;
}
```

## Insertion dans un arbre rouge noir
L'insertion se déroule de la façon suivante: #!

Comme un arbre rouge-noir est un [[ABR ou Arbre binaire de recherche]], on commence d'abord par [[ABR ou Arbre binaire de recherche#Insertion d'un élément dans un ABR|insérer l'élément à sa place]] sans tenir compte des couleurs. Le nouveau nœud est rouge, ce qui permet de ne pas changer la quantité de nœud noir sur un chemin.
Ensuite, de manière récursive, on doit rendre cette couleur rouge valide, on remonte alors de l'élément inséré jusqu'à la racine en vérifiant les propriétés. Si elles ne sont pas vérifiées, alors les couleurs changent et/ou des [[Rééquilibrage des arbres par rotation|rotations]] sont réalisées.

### Algorithme de restauration après insertion
On considère l'algorithme qui insère le nouvel élément $X$ comme indiquer puis qui restaure l'intégrité de l'arbre: #!

- **Cas 1**: Si le père de $X$ est noir, on a rien à faire, la hauteur noire n'a pas changée
- **Cas 2**: Si $X$ est la racine de l'arbre, il faut colorier $X$ en noir. C'est le seul cas où la hauteur noire augmente.
- **Cas 3:** Si $X$ a un père rouge, et qu'en plus de cela $X$ possède "un oncle" (donc un nœud ayant la même parenté que le père) rouge. Alors on colorie le père et l'oncle en noir et le grand-père en rouge. On s'intéresse maintenant à restaurer l'intégrité pour le grand-père rouge... Et donc on exécute l'algorithme sur celui-ci.
- **Cas 4**: Si le père de $X$ est rouge, mais qu'il ne possède pas d'oncle rouge, on considère les sous cas suivants:
	- **Cas 4a**: Si $X$ est un fils gauche et que son père est aussi un fils gauche. On colorie le père en noir et le grand-père en rouge puis on fait une [[Rééquilibrage des arbres par rotation|rotation droite]] du grand-père
	- **Cas 4b**: Si $X$ est un fils droit et que père est un fils gauche, on effectue une rotation gauche du père et on se ramène au cas **4a**
	- **Cas 4c**: Si $X$ est un fils droit et que le père est aussi un fils droit, on colorie le père en noir et le grand-père en rouge puis on fait une [[Rééquilibrage des arbres par rotation|rotation gauche]] du grand-père
	- **Cas 4d**: Si $X$ est un fils gauche et que son père est un fils droit, on effectue une rotation droite du père pour se ramener au cas **4c**

#### Remarque sur l'algorithme
- On réalise un appel récursif uniquement sur le cas 3 pour revérifier l'intégrité à partir du grand père.
- Des rotations ne surviennent que dans le cas 4. Donc une insertion entraine au plus 2 rotations
- Pour chaque cas on doit forcément changer la couleur d'au plus 2 nœuds. Le nombre total de changement de couleur est donc au plus 2 fois la hauteur de l'arbre
- La complexité pire cas de l'insertion est $O(log(n))$


## Suppression dans un arbre rouge noir
La suppression dans un arbre rouge-noir suit le principe général suivant: #!

Soit $n$ le nœud contenant l'élément $e$ à supprimer. Il faut assurer que l'arbre conserve les bonnes propriétés de clé:
- Si $n$ possède au plus un fils, il suffit de supprimer $n$ et de le remplacer par son fils
- Si $n$ possède deux fils, alors $n$ n'est pas supprimer, on remplace $e$ de $n$ par $e'$ l'élément le plus à gauche du sous-arbre droit. C'est le dernier nœud que l'on supprimera
Pour conserver les propriétés sur les couleurs, on procède de la manière suivante:
- Si le nœud supprimé était rouge, il n'y a rien à faire
- Si le nœud supprimé était noir, on distingue les 2 cas pathologiques suivants:
	- Si le nœud qui le remplace est rouge, alors on le colorie en noir et c'est terminer
	- Si le nœud qui le remplace est noir, on lui donne la double couleur noir et on procède à sa restauration de façon récursive.

### Algorithme de restauration après suppression
On considère l'algorithme qui supprime $X$ comme indiquer puis qui restaure l'intégrité de l'arbre: #!

- **Cas 1**: Si $X$ est une racine de l'arbre, alors on supprime la double couleur noire, et c'est le seul cas où la hauteur noir diminue
- **Cas 2**: Si le frère de $X$ est noir, alors on considère les sous-cas suivant: 
	- **Cas 2a**: Si les fils du frère de $X$ sont tous noirs, alors on colorie le frère de $X$ en rouge. Si le père de $X$ est rouge, alors on le colorie en noir, et c'est terminer. Sinon on lui attribut la double couleur noir et on restaure l'arbre à partir de lui
	- **Cas 2b**: Si le frère de $X$ est à droite et que son fils droit est rouge, alors on colorie son fils droit en noir. Ensuite, si le père de $X$ est rouge, on le colorie en noir et son frère en rouge. On termine dans tous les cas par une rotation gauche du père
	- **Cas 2c** Si le frère de $X$ est à gauche et que son fils gauche est rouge, on fait le symétrique du **2b**
	- **Cas 2d** Si le frère de $X$ est à droite et que son fils droit est noir mais que son fils gauche est rouge, on colorie le frère de $X$ en rouge et son fils gauche en noir. Puis on effectue une rotation droite du frère de $X$ pour être ramené au cas **2b**
	- **Cas 2e** Si le frère de $X$ est à gauche et que son fils gauche est noir, mais que son fils droit est rouge, on fait le symétrique de **2d**
- **Cas 3**: Si le frère de $X$ est rouge, alors on considère les sous-cas suivant: 
	- **Cas 3a**: Si le frère de $X$ est un fils droit, alors on le colorie en noir, et son père en rouge. Ensuite on effectue une rotation gauche du père. Nous sommes maintenant dans le cas **2**
	- **Cas 3b** Si le frère de $X$ est un fils gauche, alors on fait le symétrique de **3a**