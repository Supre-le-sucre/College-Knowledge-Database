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
Soit une matrice de la forme: $\begin{pmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{pmatrix}$ On observe les portraits de phases suivants: #!

- Si elles sont du même signe, positives, et que $\lambda_2 <\lambda_1$ 
  ![[Pasted image 20240620193511.png]]
- Si elles sont de même signe, positives, et que $\lambda_2 > \lambda_1$ 
  ![[Pasted image 20240620193824.png]]
- Si elles sont négatives, il suffit d'inverser les flèches
- Si la matrice est diagonalisable, il faut que les droites bleues soient dirigées par les vecteurs propres.

### Valeurs propres distinctes de signe distinct
Soit une matrice de la forme: $\begin{pmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{pmatrix}$ On observe les portraits de phases suivants: #!
- Si $\lambda_1 > 0$ 
  ![[Pasted image 20240620194231.png]]
-  Si $\lambda_1 < 0$
	![[Pasted image 20240620194302.png]]
  - Si la matrice est diagonalisable, il faut que les droites bleues soient dirigées par les vecteurs propres.
  **Observons que** $\lambda_1$ dirige l'évolution de la droite sur (Ox) comme attendu.

### Valeur propre double
Soit une matrice de la forme: $\begin{pmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{pmatrix}$ On observe les portraits de phases suivants: #!
- Si $\lambda_1 > 0$
![[Pasted image 20240620194940.png]]
- 
### Valeurs propres distinctes dont une nulle
Soit une matrice de la forme: $\begin{pmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{pmatrix}$ On observe les portraits de phases suivants: #!
- Si $\lambda_2= 0$ et $\lambda_1 > 0$
![[Pasted image 20240620195031.png]]
-  Si $\lambda_2= 0$ et $\lambda_1 < 0$: on inverse les flèches
-  Si $\lambda_1= 0$ et $\lambda_2 > 0$
![[Pasted image 20240620195117.png]]
- Si $\lambda_1= 0$ et $\lambda_2 > 0$: On inverse les flèches
- Si la matrice est diagonalisable, il faut que les droites bleues soient dirigées par les vecteurs propres.

### Valeurs propres nulles
Soit une matrice de la forme: $\begin{pmatrix} \lambda_1 & 0 \\ 0 & \lambda_2 \end{pmatrix}$ On observe le portrait de phases suivant: #!
![[Pasted image 20240620195210.png]]

## Cas diagonalisable sur $\mathbb C$
Soit une matrice de la forme: $\begin{pmatrix} \alpha & -\beta \\ \beta & \alpha \end{pmatrix}$ On observe les portraits de phases suivants: #!
- Si $\alpha > 0$ et $\beta > 0$
![[Pasted image 20240620195607.png]]
- Si $\alpha > 0$ et $\beta < 0$
![[Pasted image 20240620195719.png]]
- Si $\alpha < 0$: On change le sens des flèches
- Si $\alpha=0$ et $\beta > 0$
 ![[Pasted image 20240620195754.png]]
 - Si $\alpha=0$ et $\beta < 0$: On change le sens des flèches

## Cas trigonalisable
Soit une matrice de la forme: $\begin{pmatrix} \alpha & -\beta \\ \beta & \alpha \end{pmatrix}$ On observe les portraits de phases suivants: #!