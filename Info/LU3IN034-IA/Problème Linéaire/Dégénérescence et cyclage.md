## Définition d'une solution dégénéré
On dit qu'une solution est dégénéré dans un programme [[Méthode de Simplexe (Dantzig 1947)|simplexe]] lorsque: #!
au moins une des variables des bases est nulles.
Une solution dégénérée ne fait pas augmenter la fonction objectif au cours de l'itération.
<!--ID: 1730114115920-->


## Définition du cyclage
On dit qu'il y a un cyclage dans le programme [[Méthode de Simplexe (Dantzig 1947)|simplexe]] lorsque: #!
Au bout d'un nombre finit d'itérations, on retombe sur un dictionnaire déjà rencontré
<!--ID: 1730114115922-->


## Règle de Bland
Afin d'éviter le cyclage on applique la règle suivante: #!

A la rencontre d'une solution dégénéré, si on a le choix sur la variable entrante, on choisit toujours celle de plus petit indice
<!--ID: 1730114115924-->
