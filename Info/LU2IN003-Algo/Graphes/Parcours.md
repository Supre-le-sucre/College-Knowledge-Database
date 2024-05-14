#algo
# Graphes non orienté
## Définition
Un parcours de graphe non orienté issue de $s$ est une liste ordonnée de sommet tel que: #!

- $s$ est le premier sommet de la liste ordonnée
- chaque sommet du graphe apparaît exactement une fois
- chaque sommet suivant doit être un voisin d'un sommet déjà présent dans la liste
Il n'y a pas d'unicité du parcours. Et un graphe admet un parcours si et seulement si il est connexe.

## Sous-parcours
Un sous-parcours d'origine $s$ est définit comme étant: #! 
Un parcours dans lequel il n'est pas nécessaire d'avoir tous les sommets du graphes.

## Sommet visité
Un sommet visité $v$ est l'ensemble des sommets présent dans le sous-parcours courant.

## Bordure d'un parcours
La bordure d'un parcours est l'ensemble des sommets qui n'ont pas encore été visité mais qui ont un voisin visité dans le sous-parcours.
Ce sont tous les potentiels sommets candidats qui suivront dans le parcours.