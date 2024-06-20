# Définition
On appelle équation différentielles linéaires à coefficient constant sans second membre re en dimension 2, un système de la forme: #!
$$\begin{cases} x'(t) = ax(t) +by(t) \\ y'(t) = cx(t) + dy(t) \end{cases}$$En notant les matrices $$A = \begin{pmatrix} a & b \\ c & d\end{pmatrix} \text{ et } X(t) = \begin{pmatrix} x(t) \\ y(t) \end{pmatrix}$$On peut écrire le système comme étant: $$X'(t) = AX(t)$$
<!--ID: 1718736687568-->


# Résolutions
Remarquons que la fonction nulle est ==toujours solution== du système
La résolution de ces équations dépend de la matrice $A$

## Cas diagonale
Dans le cas diagonale, le système d'équation n'est plus complexe, et les solutions pour $x$ et $y$ sont des exponentielles simples.

## Cas triangulaire
Si la matrice est triangulaire, alors l'équation de $y$ n'est pax complexe. On résous $y$ par une exponentielle simple et on le traite comme un second membre pour $x$

## Cas non trigonalisable
Si la matrice n'est pas trigonalisable, alors elle est de la forme $$A=\begin{pmatrix}a & -b \\ b & a\end{pmatrix}$$
Il faut passer dans le plan complexe.
Dans l'espace complexe, la matrice en question sera diagonalisable et ses valeurs propres seront $\lambda = a+ib$ et $\overline \lambda$ ($a$ et $b$ sont les coefficient de la matrice $A$). Ensuite, par la matrice de passage, on retourne dans l'espace réel

## Cas général
Dans le cas générale, la solution de l'EDO est toujours $K\exp(tA)$ où $K$ est une matrice vecteur composée de deux constantes.

# Propriété sur les matrices carrée de taille 2
Toutes les matrices carrées de taille 2 sont semblables aux matrices suivantes: #!
$$D = \begin{pmatrix} a & 0 \\ 0& b \end{pmatrix} \quad T = \begin{pmatrix} a & 1 \\ 0& b \end{pmatrix}  \quad M = \begin{pmatrix} a & -b \\ b& a \end{pmatrix}$$

De fait, il existe toujours une matrice de passage $P$ telle que, pour n'importe quel matrice $A$ on a: #!
$$A = PMP^{-1}$$

## Corollaire sur la résolution
On peut donc résoudre les équations différentielles en dimension 2 simplement.
On considère l'équation $$X'=AX$$

## Cas diagonalisable
Si la matrice est diagonalisable, avec $D$ sa matrice semblable alors une solution est donnée par: #!
$$X = K\exp(tA) = KP\exp(tD)P^{-1}$$
Où $P$ est la matrice de passage, donc les colonnes sont les vecteurs propres de $A$
## Cas trigonalisable
Pour le cas trigonalisable observons déjà que: #!

La matrice $A$ est trigonalisable si son polynôme caractéristique admet deux valeurs propres communes. 
Le premier vecteur de la matrice de passage est un vecteur propre de $A$, le second est un vecteur arbitraire, non lié au premier. Il est possible de l'adapter pour obtenir le nombre que l'on souhaite dans le coin supérieur droit de la matrice triangulaire $T$ semblable à $A$.
Donc une solution serait donnée par $$X = \begin{pmatrix} C \\ D\end{pmatrix} \exp\left(t\begin{pmatrix} a & 1 \\ 0 & b\end{pmatrix}\right) = \begin{pmatrix} C \\ D\end{pmatrix} \exp\left(t\left(\begin{pmatrix} a &  0\\ 0 & b\end{pmatrix} +\begin{pmatrix} 0 &  1\\ 0 & 0\end{pmatrix}\right)\right)$$ $$X = \begin{pmatrix} C \\ D\end{pmatrix} \exp\left(t\begin{pmatrix} a & 0 \\ 0 & b\end{pmatrix}\right)\exp\left(t\begin{pmatrix} 0 & 1 \\ 0 & 0\end{pmatrix}\right)$$D'après la [[Décomposition de Dunford]] d'une matrice triangulaire

# Portrait de phase
On retient les portraits de phases suivants

## Cas diagonalisable

### Valeurs propres distinctes de même signe
On observe le portrait de phase suivant: #!
