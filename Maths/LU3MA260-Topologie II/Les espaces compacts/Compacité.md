## Définition
Un espace $(X, d)$ est dit compact si #!
Toute suite de $X$ admet une valeur d'adhérence. Autrement dit, si toute suite de $X$ admettent une sous-suite convergente 
<!--ID: 1727643554878-->


## Propriété sur la compacité d'un espace et sa fermeture
On observe la propriété suivante: #!

Soit $A \subseteq X$, Si $A$ est compact alors $A$ est fermé
Si de plus, $X$ est compact, alors toutes les parties fermées de $X$ sont compactes
<!--ID: 1727643554880-->


### Preuve
Soit $A \subseteq X$ compact, montrons qu'il est fermé

Soit $(x_n)_{n \in \mathbb N}$ une suite de $A$ convergente en $x$, montrons que $x$ est dans $A$
Comme l'espace est compact, on peut extraire une sous-suite de $(x_n)$ qui sera convergente en $A$, or comme $(x_n)$ est convergente, sa sous-suite converge au même point et donc $x \in A$

Si $(X, d)$ est compact et que l'on considère $F \subseteq X$ un fermé, montrons que $F$ est compact

On pose une suite de $(x_n)$ de $F$, donc il existe une sous-suite convergente, car il s'agit aussi d'une sous-suite de $X$ qui est compact.
Or comme $F$ est fermé et que la la sous-suite convergente est dans $F$, cette sous-suite converge dans $F$, donc $F$ est compact
$$\tag*{$\blacksquare$}$$

## Propriété: produit de deux espaces compactes
On observe que: #!

Le produit de deux epsaces compact est compact
<!--ID: 1727643554882-->


### Preuve
On pose $(X_1, d_1)$ et $(X_2, d_2)$ deux espaces compacts et $(x_n, y_n)$ une suite de $X_1 \times X_2$
Montrons qu'il existe une sous-suite convergente

Comme $X_1$ est compact, on a que $x_n$ admet une sous-suite convergente $x_{\phi_1(n)}$ vers $x$
Et $y_{\phi_1(n)}$ est une sous-suite de $X_2$, dans laquelle on peut donc extraire une sous-suite convergente (car $X_2$ est compact)
$y_{\phi_1 \circ \phi_2(n)}$ converge donc vers $y$
Donc la suite extraite de $x_{\phi_1(n)}$ qui est $x_{\phi_1(n) \circ \phi_2(n)}$ converge aussi vers $x$ (car elle est extraite d'une suite convergente en $x$)

Donc la sous-suite extraite $(x_{\phi_1(n) \circ \phi_2(n)}, y_{\phi_1(n) \circ \phi_2(n)})$ converge bien vers $(x,y)$
$$\tag*{$\blacksquare$}$$

## Propriété de la compacité sur les fonctions continues
On observe que: #!

Soit $(X, d)$ un espace compact et $f: (X, d) \to (Y, d')$ une fonction continue. Alors on a que$f(X)$ est un compact de $(Y, d')$
<!--ID: 1727643554884-->


### Preuve
Soit $(y_n)_{n \in \mathbb N}$ une suite de $f(X)$
Montrons qu'il existe une sous-suite convergente.

On sait qu'il existe $(x_n)_{n \in \mathbb N}$ de $X$ tel que $f(x_n) = y_n$. Or comme $X$ est compact, il existe une sous-suite convergente $x_{\phi(n)} \to x$
On pose alors
$$f(x_{\phi(n)}) = y_{\phi(n)}$$
Et par continuité de $f$ on a bien que
$$\lim_{n \to +\infty}y_{\phi(n)} = \lim_{n \to +\infty}f(x_{\phi(n)}) = f(x)$$
donc on a bien extrait une sous-suite convergente
$$\tag*{$\blacksquare$}$$

### Corollaire compacité entre espace homéomorphe
On observe que: #!

Si $(X,d)$ et $(Y,d')$ sont homéomorphes (i.e $f:X \to Y$ continue et admet une fonction inverse continue)
Alors $(X,d)$ est compact si et seulement $(Y,d)$ est compact
<!--ID: 1727643554885-->


#### Preuve
On rappelle que $f^{-1}$ est continu, si et seulement si, $\forall F$ fermé de $X$ $(f^{-1})^{-1}(F)$ est un fermé de $Y$

Or $f(F) = (f^{-1})^{-1}(F)$
De plus $F$ fermé de $X$ $\implies$ $F$ est compact d'après une propriété antérieur
donc $f(F)$ est compact

(Et vice-versa)
$$\tag*{$\blacksquare$}$$

### Corollaire compacité et continuité sur l'inverse
On observe le phénomène suivant: #!

Si $(X,d)$ est un compact et $f : (X, d) \to (f(X), d')$ est bijective, alors $f^{-1}$ est continue
==La réciproque est fausse==
Il existe des fonctions $f:X \to Y$ continue mais $f^{-1}$ non continue:
$f: t \to (\cos(t), \sin(t))$ $f: ([0, 2\pi[) \to \set{(x,y)\; | \; x^2 + y^2 = 1}$, on a que $f$ est continue bijective mais $f^{-1}(f^{-1}([0, \epsilon[)) = f([0, \epsilon[)$ n'est pas un ouvert dans l'espace d'arrivée 

## Compacité et complétude
On observe que: #!

Si $(X,d)$ est compact, alors il est complet
==La réciproque est fausse==
$X = (\mathbb R, |\cdot|)$ est complet, mais pas compact: (ex: $x_n = n$)
<!--ID: 1727643564375-->


### Preuve
Soit $(x_n)$ une suite de Cauchy dans $X$, montrons qu'elle converge

Comme $X$ est compact, on peut en extraire une sous-suite $x_{\phi(n)}$ qui converge vers $x$
Or comme $(x_n)$ est une suite de Cauchy on a que
$$d(x_n, x_{\phi(p)}) < \epsilon$$
Donc par passage à la limite pour $p$ on a alors que
$$d(x_n, x) < \epsilon$$
$$\tag*{$\blacksquare$}$$

