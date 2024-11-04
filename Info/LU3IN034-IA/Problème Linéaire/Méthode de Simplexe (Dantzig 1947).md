L'algorithme de simplexe est utilisé pour résoudre des [[Problème Linéaire d'optimisation|programmes linéaires]]. Il consiste à se déplacer de sommet en sommet pour atteindre un **optimum**

## Variables d'écart
Dans la méthode simplexe, on introduit des variables d'écart comme suit: #!

Chacune de ces variables transforment les inégalités du problèmes en égalité. L'objectif étant de se déplacer de sommet en sommet voisins.
<!--ID: 1730114115911-->


### Exemple
![[Pasted image 20241027175940.png]]

### Observations
Un problème ayant $m$ contraintes aura alors $m$ variables d'écarts et on a aussi que si le problèmes est composé de $(x_{1}, \dots, x_{n})$ variables, alors à chaque sommet: #!

Il y aura $n$ variables (d'écart ou non) qui seront nulles.
<!--ID: 1730114115913-->


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
<!--ID: 1730114115915-->


# Exécution de simplexe

## Par dictionnaire
Simplexe s'exécute comme suit pour un dictionnaire: #!

- A l'étape initiale, les variables de bases du problèmes sont à 0, seules les variables d'écarts sont basiques.
- On sélectionne la variable ==non basique== $x$ ayant le plus grand rapport d'augmentation dans la fonction objectif. On la fait entrer dans la base
- Par rapport à la variable non basique $x$, on vérifie laquelle variable basique $y$ a ==le plus petit rapport restrictif== par rapport à $x$ et avec un ==coefficient négatif==. Par exemple, le rapport de $y$ par rapport à $x$ tel que $y = a - bx$ est $\frac{a}{b}$. On fait alors sortir $y$ de la base
<!--ID: 1730114115917-->


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

Dans ce dictionnaire, les variables basiques sont $s_{1}, s_{2}$ et $s_{3}$, et les variables non basiques sont $x_{1}$ et $x_{2}$
Dans cette situation, $x_{2}$ a le plus grand rapport d'augmentation d'objectif (il a un coefficient égal à $6$, alors que le coefficient de $x_{1}$ est de $1$)
==**NOTONS QUE**==: si l'objectif était une minimisation, on aurait voulu prendre le plus petit coefficient !

$x_{2}$ va donc entrer dans la base... Sélectionnons la variable basique ayant le plus petit rapport de contrainte avec $x_{2}$:
- $s_{1}$ a un rapport infini: $s_{1} = 200 - x_{1} + 0x_{2}$, le rapport est donc $\frac{200}{0} = \infty$
- $s_{2}$ a un rapport de $\frac{300}{1} = 300$
- $s_{3}$ a un rapport de $\frac{400}{1} = 400$
C'est donc $s_{2}$ qui va devenir non-basique, car c'est elle qui a le rapport de contrainte le plus faible
Donc...
On rends $s_{2}$ non basique soit $s_{2} = 0$, donc on a que $x_{2} = 300$. Le reste des valeurs ne changent pas: $s_{1} = 200, s_{3} = 400, x_{1}=0$

Le second dictionnaire est alors
$$
\begin{align*}
s_{1}& = 200 - x_{1} & s_{1} &= 200-x_{1} & s_{1} & = 200 - x_{1}\\
x_{2}& = 300 - s_{2} & \implies x_{2} &=300 - s_{2} & \implies x_{2} & = 300 - s_{2}\\
s_{3}& = 400 - x_{1} - x_{2} & s_{3} &=400 - x_{1} - (300-s_{2}) & s_{3} & = 100 - x_{1} +s_{2} \\
\_\_&\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ & \_\_&\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ & \_\_&\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  \\
z&=x_{1} + 6x_{2} & z & = x_{1} + 6(300-s_{2}) & z & = 1800 +x_{1} -6s_{2}
\end{align*}
$$
Maintenant $x_{1}$ est la variable qui augmentera l'objectif, et le plus petit rapport est en $s_{3}$

Donc on a $s_{3} = 0$, donc $x_{1} = 100 +s_{2} = 100 + 0 = 100$ car en effet $s_{2} = 0$. Les autres variables sont inchangées $s_{2} = 0, s_{1} =200, x_{2} = 300$

D'où le troisième dictionnaire:
$$\begin{align*}
s_{1}& = 200 - x_{1} & s_{1} &= 200 - (100+ s_{2} -s_{3}) & s_{1} &= 100 - s_{2} + s_{3}\\
x_{2}& = 300 - s_{2} & x_{2} &= 300 - s_{2} &  x_{2}&=300 - s_{2} \\
x_{1}& = 100 + s_{2} -s_{3} &  x_{1} & = 100 + s_{2} -s_{3} & x_{1} &= 100 + s_{2} -s_{3}\\
\_\_&\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ & \_\_&\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ & \_\_&\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\\
z&=1800 + x_{1} - 6s_{2} & z&=1800 + (100 + s_{2}-s_{3}) - 6s_{2} & z&= 1900 - 5s_{2} -s_{3}
\end{align*}$$

Le troisième dictionnaire nous montrer bien qu'il est impossible d'améliorer l'objectif: les coefficients sont tous négatif
==**NOTONS QUE**==: Les coefficient devrait être tous positifs s'il s'agissait d'une minimisation

On a donc que $z= 1900$, c'est le meilleur résultat possible...
Pour l'obtenir, on a donc $x_{1} = 100$ et $x_{2} = 300$

## Méthode matricielle
La méthode matricielle est la même que celle posant le dictionnaire, elle est plus efficace dans les grands problèmes car il ne faut pas réécrire toutes les variables

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

On pose alors le système
$$
\begin{align}
&+x_{1} & & + s_{1} & & &&=200 \\
&& +x_{2} & & +s_{2} & & &=300 \\ \\
&+x_{1} &+x_{2} & & & +s_{3} &&= 400 \\ \\
-z & +x_{1} + 6x_{2} & & & & & &= 0
\end{align}
$$

Ceci donne la matrice dictionnaire suivante
$$
\begin{pmatrix}
1&0&1&0&0&200 \\
0&1&0&1&0&300 \\
1&1&0&0&1&400 \\
1&6&0&0&0&0
\end{pmatrix}
$$

>On examine alors tous les nombres de la dernière ligne. La colonne ayant le nombre le plus grand sur cette ligne est alors sélectionnée, c'est la **colonne de pivot** (c'est l'homologue de sélection de la variable entrante)

Dans notre exemple, c'est la deuxième colonne qui respecte cette condition
$$
\begin{pmatrix}
1&\mathbf{0}&1&0&0&200 \\
0&\mathbf{1}&0&1&0&300 \\
1&\mathbf{1}&0&0&1&400 \\
1&\mathbf{6}&0&0&0&0
\end{pmatrix}
	$$

> On regarde ensuite, la colonne en ne regardant que les lignes avec ==un coefficient strictement positif==.
   En posant $s$ la donnée la plus à droite de la ligne et $r$ le coefficient sur la colonne de pivot, on sélectionné la **ligne de pivot** telle que le rapport $\frac{s}{r}$ est minimum. (c'est l'homologue de la sélection de notre variable sortante)

Dans notre exemple, c'est la deuxième ligne qui respecte cette condition
$$
\begin{pmatrix}
1&\mathbf{0}&1&0&0&200 \\
\mathbf{0}&\mathbf{1}&\mathbf{0}&\mathbf{1}&\mathbf{0}&\mathbf{300} \\
1&\mathbf{1}&0&0&1&400 \\
1&\mathbf{6}&0&0&0&0
\end{pmatrix}
$$

Le **nombre de pivot** est l'intersection entre la colonne et la ligne de pivot, dans notre exemple, ce nombre vaut $\mathbf{1}$ 

> On divise maintenant chaque entrées de la ligne de pivot par $\mathbf{1}$, le nombre de pivot

$$
\begin{pmatrix}
1&{0}&1&0&0&200 \\
\mathbf{\frac{0}{1}}&\mathbf{\frac{1}{1}}&\mathbf{\frac{0}{1}}&\mathbf{\frac{1}{1}}&\mathbf{\frac{0}{1}}&\mathbf{\frac{300}{1}} \\
1&{1}&0&0&1&400 \\
1&{6}&0&0&0&0
\end{pmatrix} = 
\begin{pmatrix}
1&{0}&1&0&0&200 \\
\mathbf{{0}}&\mathbf{1}&\mathbf{0}&\mathbf{1}&\mathbf{0}&\mathbf{300} \\
1&{1}&0&0&1&400 \\
1&{6}&0&0&0&0
\end{pmatrix}
$$

> Puis on soustrait à chaque ligne, la ligne de pivot, de sorte que la colonne de pivot ne soit composée que de 0 à l'exception du nombre de pivot

Dans notre exemple $L_{1}$ ne change pas, car le coefficient de la colonne de pivot est déjà nul en revanche, toutes les autres lignes changent: $L_{3} \leftarrow L_{3} - L_{2}$ et $L_{4} \leftarrow L_{4} - 6L_{2}$
$$
\begin{pmatrix}
1&{0}&1&0&0&200 \\
{0}&{1}&{0}&{1}&{0}&{300} \\
\mathbf{1}&\mathbf{0}&\mathbf{0}&\mathbf{-1}&\mathbf{1}&\mathbf{100} \\
\mathbf{1}&\mathbf{0}&\mathbf{0}&\mathbf{-6}&\mathbf{0}&\mathbf{-1800}
\end{pmatrix}
$$

> On continue le procédé jusqu'à ce que tous les coefficient de la dernière ligne soit négatifs (ou positif si le problème est un problème de minimisation !!)

$$
\begin{pmatrix}
1&0&1&0&0&200 \\
0&1&0&1&0&300 \\
1&0&0&-1&1&100 \\
1&0&0&-6&0&-1800
\end{pmatrix} \xrightarrow[L_{1} \leftarrow L_{1} - L_{3}, \; L_{4} \leftarrow L_{4} - L_{3}]{L_{3} \text{ ligne de pivot}}
\begin{pmatrix}
0&0&1&1&0&100 \\
0&1&0&1&0&300 \\
1&0&0&-1&0&100 \\
0&0&0&-5&-1&-1900
\end{pmatrix}
$$

On peut ensuite conclure, en reprenant le système de base que $-z = -1900$ donc $z=1900$ est notre solution optimale.
Et que $x_{1} = 100$ d'après la première colonne et $x_{2} = 300$ d'après la seconde colonne