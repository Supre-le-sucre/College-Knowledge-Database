# Méthode en dimension 1
Pour montrer le fonctionnement de la variation de la constante, nous allons explorer l'équation différentielle classique générale: 
$$ax' = bx + c \quad (1)$$
(On aurait pu aussi prendre $c$ comme étant une fonction, la méthode est la même)
## Etape 1: Résolution sans second membre
D'abord, on essaye de résoudre l'équation sans second membre. On cherche donc à résoudre
$$ay' = by \quad (2)$$

Le résultat de cet équation est connu:
$$ay' = by \; \Leftrightarrow \; y' = \frac{b}{a}y \; \Leftrightarrow \;  y=\lambda e^{\frac{b}{a}t}$$

## Etape 2: Résolution par variation de la constante
Maintenant que l'on connaît le résultat pour $(2)$, on va considérer que sa constante est une fonction et admettre que la solution de $(1)$ s'écrit de la forme:
$$x(t) = \lambda(t)y(t)$$
Où $y(t)$ la solution de l'équation $(2)$ et $\lambda(t)$ une fonction que l'on déterminera
Observons déjà que
$$x'(t) = \lambda'(t)y(t) + \lambda(t)y'(t)$$

Or comme $y$ est solution de l'équation $(2)$ on a que
$$y' = \frac{b}{a}y$$
Donc on a que
$$x'(t) = y(t)\left(\lambda'(t) + \frac{b}{a}\lambda(t)\right)$$

Or on considère l'équation $(1)$
$$a x' = bx +c \Leftrightarrow ay(t)\left(\lambda'(t) + \frac{b}{a}\lambda(t)\right) = b\lambda(t)y(t) + c$$
$$\Leftrightarrow ay(t)\lambda'(t) + by(t)\lambda(t) = b\lambda(t)y(t) +c$$
$$\Leftrightarrow ay(t)\lambda'(t) = c$$

Or on connaît déjà la valeur de $y(t)$, donc on peut en déduire la valeur de $\lambda'(t)$ car $y(t)$ ne s'annule jamais (c'est la fonction exponentielle)
$$\lambda'(t) = \frac{c}{a}\frac{1}{y(t)} =\frac{c}{a} e^{-\frac{b}{a}t}$$

Donc on a que, en prenant la primitive de $\lambda'$
$$\lambda(t) = -\frac{c}{b}e^{-\frac{b}{a}t} + K \quad | \; K \in \mathbb R$$
Finalement les solutions de l'équation $(1)$ seront donnée par
$$x(t) = \lambda(t)y(t) = \left(-\frac{c}{b}e^{-\frac{b}{a}t} + K\right)e^{-\frac{b}{a}t}$$
$$x(t) = Ke^{-\frac{b}{a}t} - \frac{c}{b}$$
$$\tag*{$\blacksquare$}$$

