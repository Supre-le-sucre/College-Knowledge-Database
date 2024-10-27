L'algorithme de simplexe est utilisé pour résoudre des [[Problème Linéaire d'optimisation|programmes linéaires]]. Il consiste à se déplacer de sommet en sommet pour atteindre un **optimum**

## Variables d'écart
Dans la méthode simplexe, on introduit des variables d'écart comme suit: #!

Chacune de ces variables transforment les inégalités du problèmes en égalité. L'objectif étant de se déplacer de sommet en sommet voisins.

### Exemple
![[Pasted image 20241027175940.png]]

### Observations
Un problème ayant $m$ contraintes aura alors $m$ variables d'écarts et on a aussi que si le problèmes est composé de $(x_{1}, \dots, x_{n})$ variables, alors à chaque sommet: #!

Il y aura $n$ variables (d'écart ou non) qui seront nulles.

#### Exemple
![[Pasted image 20241027180309.png]]

## Définitions
Lors du déroulement de simplexe, les variables prennent des noms particuliers, dont voici la définition:

- **Variable non basique**: Une variable mise à zéro
- **Variable basique**: Une variable non nulle
- **Base**: L'affectation courante des variables à un moment donné de l'algorithme simplexe

## Propriété sur la base courante et les variables
Dans l'algorithme de simplexe, lorsque deux sommets sont voisins on observe que: #!

Les ensembles de variables basiques et non basiques sont les mêmes à l'exception d'un seul et unique élément.
Le processus de simplexe consiste alors à échanger une paire de variable de l'ensemble basique à l'ensemble non basique

# Exécution de simplexe

## Par dictionnaire
Simplexe s'exécute comme suit pour un dictionnaire: #!

- A l'étape initiale, les variables de bases du problèmes sont à 0, seules les variables d'écarts sont basiques.
- On sélectionne la variable ==non basique== $x$ ayant le plus grand rapport d'augmentation dans la fonction objectif. On la fait entrer dans la base
- Par rapport à la variable non basique $x$, on vérifie laquelle variable basique $y$ a ==le plus petit rapport restrictif== par rapport à $x$. Par exemple, le rapport de $y$ par rapport à $x$ tel que $y = a + bx$ est $\frac{a}{b}$. On fait alors sortir $y$ de la base

### Exemple
On considère le problème linéaire suivant
$$
\begin{cases}
\max x_{1} + 6x_2  \\ \\
x_{1} \leq 200 \\
x_{2} \leq 300 \\
x_{1} + x_{2} \leq 400 \\ \\
x_1, x_{2} \geq 0 
\end{cases} \quad \xRightarrow{\text{Création des variables d'écarts}} \quad
\begin{cases}
\max z = x_{1} + 6x_2  \\ \\
x_{1} +s_{1} = 200 \\
x_{2} + s_{2} = 300 \\
x_{1} + x_{2} + s_{3} = 400 \\ \\
x_1, x_{2}, s_{1}, s_{2}, s_{3} \geq 0 
\end{cases}
$$
On pose alors le premier dictionnaire où $x_{1} = x_{2} = 0$
$$
\begin{align*}
s_{1}& = 200 - x_{1} \\
s_{2}& = 300 - x_{2} \\
s_{3}& = 400 - x_{1} -x_{2} \\
\_\_&\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\ \\
z&=x_{1} + 6x_{2}
\end{align*}

$$