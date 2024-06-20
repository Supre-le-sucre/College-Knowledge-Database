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
Dans le cas générale, la solution de l'EDO est toujours $\exp(tA)$

# Propriété sur les matrices carrée de taille 2
Toutes les matrices carrées de taille 2 sont semblables aux matrices suivantes: #!
$$D = \begin{pmatrix} a & 0 \\ 0& b \end{pmatrix} \quad T = \begin{pmatrix} a & 0 \\ 0& b \end{pmatrix} $$


