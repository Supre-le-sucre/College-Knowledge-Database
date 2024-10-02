
## Dégénérescence
Un dictionnaire est dégénéré: #!
S'il admet au moins un coefficient nul sur une variable de base.
Dans ce cas, la valeur de la fonction objectif restera la même.

## Cyclage
On dit que l'on aboutit à un cyclage: #!
Si on retombe sur un dictionnaire déjà rencontré

### Règle de Bland
On peut éviter le cyclage de la façon suivante: #!
A toute itération d'un dictionnaire dégénéré, lorsqu'on a le choix sur la variable entrante ou sortante, on prends toujours celle d'indice (donc de coefficient) plus faible.
