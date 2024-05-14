#algo

## Définition
Un arbre est un [[Graphes non orientés]] connexe acyclique (i.e sans [[Graphes non orientés#Chaînes particulières|Cycle]])

## Minimal connexe et Maximal acyclique
### Minimal connexe

On dit d'un [[Graphes non orientés]] qu'il est minimal connexe s'il est connexe, et que si l'on retire n'importe quel arête du graphe, il n'est plus connexe (i.e $\forall e \in E, G' = (V, E\setminus\set{e}$ non connexe)

### Maximal acyclique
On dit d'un [[Graphes non orientés]] qu'il est maximal acyclique si $G$ est sans cycle élémentaire, mais que rajouter une nouvelle arête entraîne la création d'un cycle.
(i.e pour tout couple de sommets $\set{x, y}$ non adjacents dans $G$. On a que $G' = (V, E \cup \set{\set{x, y}}$ contient un cycle)

## Théorème
Soit $T = (V, E)$ un [[Graphes non orientés]], alors les assertions suivantes sont équivalentes:
- T est un arbre
- T est minimal connexe
- T est maximal acyclique
- Entre deux sommets quelconques, il existe une chaîne élémentaire unique.
