#algo
# [[Graphes non orientés]]
## Définition
Un parcours de graphe non orienté issue de $s$ est une liste ordonnée de sommet tel que: #!

- $s$ est le premier sommet de la liste ordonnée
- chaque sommet du graphe apparaît exactement une fois
- chaque sommet suivant doit être un voisin d'un sommet déjà présent dans la liste
Il n'y a pas d'unicité du parcours. Et un graphe admet un parcours si et seulement si il est connexe.
<!--ID: 1715702538727-->


## Sous-parcours
Un sous-parcours d'origine $s$ est définit comme étant: #! 
Un parcours dans lequel il n'est pas nécessaire d'avoir tous les sommets du graphes.
<!--ID: 1715702538730-->


## Sommet visité
Un sommet visité $v$ par le sous-parcours $L$ lorsque: #!
$v \in L$. On note d'ailleurs $V(L)$ l'ensemble des sommets visité par $L$
<!--ID: 1715702538732-->


## Bordure d'un sous-parcours
La bordure d'un sous-parcours est: #!
L'ensemble des sommets qui n'ont pas encore été visité mais qui ont un voisin visité dans le sous-parcours.
Ce sont tous les potentiels sommets candidats qui suivront dans le parcours. On le note mathématiquement: $$\mathcal B(L) = \set{v \in V - V(L) \; | \; \exists \set{u,v} \in E, u \in L}$$
<!--ID: 1715702538738-->


## Sommet ouvert et fermé
Soit $L$ un sous-parcours. On dit qu'un sommet visité $v \in V(L)$ est ouvert si: #!

Il possède au moins un sommet adjacent qui n'est pas dans $L$ (donc un sommet dans $\mathcal B(L)$).
Si ce n'est pas le cas alors le sommet visité est dit *"fermé"*
<!--ID: 1715702538747-->


## Graphe de liaison
On donne $\mathcal A(L)$ le graphe de liaison associé au [[#Sous-parcours]] $L$ d'un [[Graphes non orientés]] $G=(V, E)$ tel que: #!

$\mathcal A(L) = (V(L), H(L))$ est un [[Graphes orientés]], avec, $V(L)$ l'ensemble des [[#Sommet visité]] et $H(L)$ définit mathématiquement comme étant: $$H(L) = \set{(u, v) \; | \; u < v \text{ dans L, et } \set{u,v} \in E}$$
<!--ID: 1715702538756-->


### Théorème sur le graphe de liaison
Soit $G=(V, E)$ et un $L$ un parcours de $G$ d'origine $s \in V$ alors on a que: #!

$s$ est une [[Graphes orientés#Définition de la racine|racine]] du graphe de liaison $\mathcal A(L)$
<!--ID: 1715702538765-->


## Implémentation d'un parcours générique
L'implémentation d'un parcours générique d'un graphe $G$ d'origine $s$ se fait de la façon suivante:

```
L := (s), B := B(L) <- B est la bordure de L
while B not empty:
	pick u in B
	L := L + (u)
	B := B(L)
end while
```

## Connexité d'un graphe en fonction du parcours
On observe la propriété suivante: #!
On a qu'un graphe $G$ est connexe si et seulement s'il existe un parcours de $G$
<!--ID: 1715702538775-->


# [[Graphes orientés]]

## Définition
Un parcours de graphe orienté issue de $s$ est une liste ordonnée de sommet tel que: #!

- $s$ est le premier sommet de la liste ordonnée
- chaque sommet du graphe apparaît exactement une fois
- chaque sommet suivant doit être un successeur d'un sommet déjà présent dans la liste
<!--ID: 1715702538782-->


