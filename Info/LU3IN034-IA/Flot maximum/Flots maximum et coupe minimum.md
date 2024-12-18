# Théorème de la coupe minimum
Les assertions suivantes sont équivalentes: #!

i) $f$ est un [[Flots#Définition du flot maximum|flot maximum]] de $G= (V, E, c)$
ii) Il existe une [[Coupe|coupe]], appelée coupe maximum $(A, B)$ de [[Coupe#Capacité d'une coupe|capacité]] $c(A, B) = |f|$
iii) Il n'existe pas de [[Graphes d'écart (ou résiduel)#Définition|chemin augmentant]] dans $G_f$
<!--ID: 1730114115959-->



# Algorithme de Ford & Fulkerson
L'algorithme cherche à établir un [[Flots|flot]] maximum dans un graphe $G$: #!

**Etape I** On commence avec un flot $f = 0$ dans $G$
**Etape II** On choisit un chemin augmentant $p$ dans $G_f$ et on pousse $d$ unités supplémentaires de $s$ à $t$ (avec $d$ la capacité [[Graphes d'écart (ou résiduel)|résiduelle]] ==minimale== entre les arcs)
**Etape III** On répète ça jusqu'à ce qu'il n'existe plus de chemin augmentant sur $G_f$
<!--ID: 1730114115961-->


## Complexité
La complexité de l'algorithme de Ford et Fulkerson est tel que: #!
Le flot maximum est obtenu au bout d'au plus $O(|f^*|)$ étapes d'augmentation
<!--ID: 1730114115963-->


## Exemple d'exécution
![[Pasted image 20241026200622.png]]
![[Pasted image 20241026200803.png]]
On observe qu'il n'y a pas de chemin liant $s$ à $t$ dans le dernier graphe d'écart. Cela signifie donc qu'il n'y a pas de chemin augmentant. Nous avons donc trouver le flot maximum $f^*$ dont la valeur de flot $|f^*| = 12$
*==Note importante:== à partir de la deuxième étape, on peut observer un flot négative de $v$ vers $u$, c'est parce que le flot est antisymétrique, donc il doit garder cette propriété*

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
<!--ID: 1730114115965-->


## Trouver la coupe minimum
Pour trouver la [[Coupe|coupe]] minimum d'un [[Graphes de capacité|graphe]] $G=(V, E, c, s, t)$ en connaissant son flot maximum $f^*$: #!

**Etape I** On pose le graphe d'écart $G_{f^*}$
**Etape II** On détermine $A$, l'ensemble des sommets que l'on peut atteindre à partir de $s$ dans $G_{f^*}$
**Etape III** On détermine $B = V\setminus A$
On a alors que $(A, B)$ qui est une coupe minimum
<!--ID: 1730114115966-->


# Algorithme de Edmonds-Karp
L'algorithme d'Edmonds-Karp pour déterminer un flot maximum est tel que: #!

Il s'agit du même algorithme que Ford & Fulkerson à l'exception que le choix du chemin augmentant n'est plus arbitraire. On décide de prendre le [[Graphes d'écart (ou résiduel)#Chemin critique|chemin critique]].
L'avantage de cette algorithme, c'est que l'on trouvera plus efficacement la valeur du flot maximum
<!--ID: 1730114115968-->


## Complexité de l'algorithme
### Propriété sur la capacité résiduelle d'un chemin critique
Dans un [[Graphes de capacité|graphe]] $G = (V, E, c)$ de flot maximum $f^*$, le [[Graphes d'écart (ou résiduel)#Chemin de capacité critique|chemin critique]] $p^*$ a une capacité résiduelle d'au moins: #!
$$c(p^*) \geq \frac{|f|}{|E|}$$
<!--ID: 1730114115970-->


### Nombre d'itérations
L'algorithme de Edmonds-Karp augmente le flot autant de fois que:  #!
$$O(|E| \log(|f^*|))$$
Avec $f^*$ un flot maximum
<!--ID: 1730114115971-->


### Complexité finale
La complexité finale de l'algorithme de Edmonds-Karp est en: #!
$$O( | E |^2 \log(n) \log(|f^*|))$$
Car on trouve un chemin critique au bout de $O(|E| \log(n))$ itérations.
<!--ID: 1730114115973-->


## Exemple
![[Pasted image 20241026203943.png]]
On choisira ici le chemin augmentant $s-u-t$. Dans l'autre algorithme, on aurait pu choisir parmi tous les autres.
*==Note importante:== Sur le graphe de départ, on peut observer un flot négative de $v$ vers $u$, c'est parce que le flot est antisymétrique, donc il doit garder cette propriété. Ce qu'il se passe de v vers u est donc expliciter, ce qui fait que le graphe d'écart n'a pas d'arcs en plus*

## Algorithme d'Edmonds-Karp II
Quelle chemin augmentant faut-il prendre s'il existe plusieurs chemin critique ? #!

On prends alors le chemin critique ayant le nombre d'arcs minimum. Pour cela, on effectue un [[Parcours en largeur#Implémentation d'un parcours en largeur|parcours en largeur avec évaluation des distances]]
<!--ID: 1730114115975-->


### Définition d'un arc avant
Un arc $(u,v)$ est qualifié d'arc avant dans un parcours en largeur si: #!

Il existe $i$ tel que $u \in V_i$ et $v \in V_{i+1}$. Avec $V_{i}$ l'ensemble des sommets à distances $i$ de $s$ dans $G$
<!--ID: 1730114115976-->


#### Analyse de l'algorithme
En utilisant l'algorithme d'Edmonds-Karp, on observe un phénomène intéressant sur les arcs avant: #!

L'algorithme va saturer au moins un arc-avant qui va disparaître alors dans le prochain graphe d'écart.
Cela signifie donc que la distance $d$ de $s$ à $t$ ne ==diminue jamais==, mais ==ne fait qu'augmenter==. Toutes les $|E|$ itérations (car on évalue chaque chemin de $s$ à $t$), $d$ incrémente d'au moins $1$ et ceci peut se faire au plus $|V|$ fois (chaque sommet pourrait être invalidés à la fin).
Le nombre d'itérations de cet algorithme est donc d'au plus $$O(|V| \cdot |E|)$$
### Complexité de l'algorithme d'Edmonds-Karp II
Le flot maximum est alors obtenu en: #!
$$O(|E|^2 \cdot |V|)$$
(Car un parcours en largeur se fait en $O(|E| + |V|) = O(|E|)$)
<!--ID: 1730114115978-->


