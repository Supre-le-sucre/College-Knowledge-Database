# Théorème de la coupe minimum
Les assertions suivantes sont équivalentes: #!

i) $f$ est un [[Flots#Définition du flot maximum|flot maximum]] de $G= (V, E, c)$
ii) Il existe une [[Coupe|coupe]], appelée coupe maximum $(A, B)$ de [[Coupe#Capacité d'une coupe|capacité]] $c(A, B) = |f|$
iii) Il n'existe pas de [[Graphes d'écart (ou résiduel)#Définition|chemin augmentant]] dans $G_f$


# Algorithme de Ford & Fulkerson
L'algorithme cherche à établir un [[Flots|flot]] maximum dans un graphe $G$: #!

**Etape I** On commence avec un flot $f = 0$ dans $G$
**Etape II** On détermine un chemin augmentant $p$ dans $G_f$ et on pousse $d$ unités supplémentaires de $s$ à $t$ (avec $d$ la capacité [[Graphes d'écart (ou résiduel)|résiduelle]] ==minimale== entre les arcs)
**Etape III** On répète ça jusqu'à ce qu'il n'existe plus de chemin augmentant sur $G_f$

## Complexité
La complexité de l'algorithme de Ford et Fulkerson est tel que: #!
Le flot maximum est obtenu au bout d'au plus $O(|f^*|)$ étapes d'augmentation
<!--ID: 1726076885898-->

## Exemple d'exécution
![[Pasted image 20241026200622.png]]
![[Pasted image 20241026200803.png]]
On observe qu'il n'y a pas de chemin liant $s$ à $t$ dans le dernier graphe d'écart. Cela signifie donc qu'il n'y a pas de chemin augmentant. Nous avons donc trouver le flot maximum $f^*$ dont la valeur de flot $|f^*| = 12$

## Marquage de Ford & Fulkerson
Pour ne pas utiliser de graphe d'écart on utile l'algorithme de marquage suivant: #!

```
marquer s d'un +
	répéter jusqu'à ce que t soit marqué
		Si il existe e = (u,v) avec u marqué et v non marqué et f(e) < c(e)
			alors marquer v d'un + et père(v) <- u
		Sinon
			Si il existe e = (u,v) avec v marqué et u non marqué et f(e) > 0
			alors marquer u d'un - et père(u) <- v
```
Le père d'un sommet est son père dans le graphe d'écart.
Un sommet est marqué d'un $+$ si son père peut encore lui donner un flot supplémentaire. Il est marqué d'un $-$ s'il ne peut donner de flot supplémentaire.

## Trouver la coupe minimum
Pour trouver la [[Coupe|coupe]] minimum d'un [[Graphes de capacité|graphe]] $G=(V, E, c, s, t)$ en connaissant son flot maximum $f^*$: #!

**Etape I** On pose le graphe d'écart $G_{f^*}$
**Etape II** On détermine $A$, l'ensemble des sommets que l'on peut atteindre à partir de $s$ dans $G_{f^*}$
**Etape III** On détermine $B = V\setminus A$
On a alors que $(A, B)$ qui est une coupe minimum

