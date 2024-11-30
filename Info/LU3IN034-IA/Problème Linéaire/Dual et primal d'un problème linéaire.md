
On considère ici le programme linéaire primal canonique $\mathcal P$ avec
- $X = \begin{pmatrix} x_{1} \\ \vdots \\ x_{n} \end{pmatrix}$  les variables du problème
- $b = (b_{1}, \cdots ,b_{n})$ les coefficients de la fonction objectif
- $A= \begin{pmatrix} a_{1,1} & \cdots & a_{1,n} \\ \vdots & \ddots & \vdots \\ a_{p,1} & \cdots & a_{p,n}\end{pmatrix}$ les coefficients de contraintes
- $c = \begin{pmatrix} c_{1} \\ \vdots \\ c_{p} \end{pmatrix}$ le vecteur de contraintes linéaire

Le problème peut alors se formuler de la façon suivante
$$
\begin{align}
\text{Objectif:}& \quad \min z = bX  \\
\mathcal P : & \quad AX \geq c \\
& \quad X \geq 0
\end{align}
$$
On aurait pu aussi maximiser $\mathcal P$

## Dual du problème $\mathcal P$
On appelle dual au problème de minimisation canonique $\mathcal P = (X, A, b, c)$ le problème $\mathcal D$ suivant: #!
$$
\begin{align}
\text{Objectif:}& \quad \max z = cV  \\
\mathcal D : & \quad ^tAV \leq b \\
& \quad V \geq 0
\end{align}
$$
Où $V$ est le vecteur de variable du problème $\mathcal D$ de taille $p$ (le nombre de contrainte du problème $\mathcal P$). Si $\mathcal P$ était un problème de maximisation, $\mathcal D$ aurait été un problème de ==minimisation== et les inégalités aurait aussi changé de sens.

## Observations préliminaires
Par rapport au problème primal $\mathcal P$, le problème dual $\mathcal D$ présente les caractéristiques suivantes: #!

- Si $\mathcal P$ est un problème de maximisation (resp. min) alors $\mathcal D$ sera un problème de minimisation (resp. max)
- Le dual $\mathcal D$ présente autant de variables que $\mathcal P$ n'a de contraintes
- Le dual $\mathcal D$ présente autant de contraintes que $\mathcal P$ n'a de variables
- Les coefficients de la fonction objectif de $\mathcal D$ sont les seconds membres des inégalités de $\mathcal P$
- Les second membre des inégalités de $\mathcal D$ sont les coefficients de la fonction objectif de $\mathcal P$
- Les lignes de la matrice de contrainte de $\mathcal D$ sont les colonnes de celle de $\mathcal P$
- ==A l'optimum, les fonctions objectifs ont des valeurs égales==
- ==Le dual du dual est le problème primal==

## Cas du dual dans les problèmes généraux
Dans le cas où un problème $\mathcal P$ n'est plus canonique, il faut que son dual $\mathcal D$ soit correctement arrangé.