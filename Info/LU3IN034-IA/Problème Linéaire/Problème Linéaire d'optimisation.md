# Définition
On définit un problème linéaire d'optimisation de la façon suivante: #!

Un problème linéaire est un problèmes ayant un ensemble de contraintes linéaires (égalité ou inégalité). Et dont la fonction objective d'un tel problème peuvent être le maximum ou le minimum d'une application linéaire.
<!--ID: 1727256183774-->


## Représentation géométrique
Les problèmes linéaire d'optimisation peuvent se représenter géométriquement, en particulier s'il n'y a pas plus de 3 variables.
Chaque variable représente un axe, et les contraintes définissent l'ensemble d'étude: en faisant l'intersection de tous les espaces contraints.

En règle générale, l'optimum se trouve dans un des sommets de la région réalisables.

### Determination d'un sommets de manière algébrique
Les sommets de notre ensemble d'étude sont: #!
les contraintes d'inégalité transformée en égalités. Pour établir cela, il nous faut des variables d'écart, qui seront à 0 à un sommet. En fonction de la dimension du problème, on doit avoir suffisamment de variables d'écart de tel sorte à ce qu'il y ait autant de variables à 0 que de dimension sur un sommet.

## Exceptions aux PL
Si la région de résolution représente une intersection vide, alors le problèmes est irréalisable.
DE même si l'espace de résolution n'est pas majoré dans le cas d'une maximisation, ou minoré dans le cas du minimisation, alors le problème est irréalisable.