Parfois en utilisant la méthode [[Méthode de Simplexe (Dantzig 1947)|de Simplexe]], on ne peut pas tomber sur un dictionnaire réalisable en mettant les variables de bases à 0.

## Problème auxiliaire
Pour obtenir un dictionnaire réalisable, on poser un problème auxiliaire: #!

L'objectif devient $\max w = -x_0$ (ce qui revient à minimiser $x_{0}$). On pose alors $-x_{0}$ sur chaque contrainte (ou seulement sur les contraintes problématiques pour simplifier.
On fait sortir continuellement les variables les plus négatives de la base lorsque le dictionnaire n'est pas réalisable.
Lorsque $w$ est maximisé et qu'il vaut $0$, on a alors une solution réalisable de l'autre côté. C'est à partir de celle-ci que l'on pourra commencer la méthode [[Méthode de Simplexe (Dantzig 1947)|de Simplexe]]. S'il ne vaut pas $0$, alors le problème initial n'admet pas de solution !
