Une file de priorité est une [[Files]], qui n'est pas FIFO, mais qui fait sortir les éléments prioritaire en premier, puis le reste en FIFO.

## Définition
On définit une file de priorité de la façon suivante: #!

Ce type de données représente un ensemble de données homogène chacune associée à une valeur, son niveau de priorité. Une file de priorité permet l'extraction d'élément de priorité minimal ou maximal et l'ajout aisé de nouvelles données.
On tient à avoir ces opérations classiques:
- `Ajouter(x, p, F)` ajoute $x$ avec une priorité $p$ à la file $F$
- `ExtraireMin(F)` sort l'élément avec la plus petit priorité de $F$
- `Fusionner(F1, F2)` fusionne les files $F_1$ et $F_2$ 
