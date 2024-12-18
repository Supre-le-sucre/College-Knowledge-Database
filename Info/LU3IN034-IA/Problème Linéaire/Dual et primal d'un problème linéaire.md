	
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
<!--ID: 1734268137939-->


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
<!--ID: 1734268137941-->


## Cas du dual dans les problèmes généraux
Dans le cas où un problème $\mathcal P$ n'est plus canonique, il faut que son dual $\mathcal D$ soit correctement arrangé: #!

Dans un problème $\mathcal P$ de maximisation
- Si une contrainte est de la forme $\leq$ la variable du dual sera signée ($\geq 0$) et le second membre sera exprimé positivement dans la fonction objectif
- Si une contrainte est de la forme $=$, la variable du dual sera non signée et le second membre sera exprimé positivement dans la fonction objectif
- Si une contrainte est de la forme $\geq$, la variable du dual sera signée ($\geq 0$) et le second membre sera exprimé **négativement** dans la fonction objectif
Dans un problème $\mathcal P$ de minimisation, la variable du second membre aura le signe inverse dans le dual.
<!--ID: 1734268137942-->


### Exemple
![[Pasted image 20241130111956.png]]

## Propriété sur les solutions réalisables du dual et primal
Si $X$ est une solution réalisable du primal $\mathcal P$, et $V$ une solution réalisation du dual $\mathcal D$ alors: #!

$$
bX  \leq cV
$$
<!--ID: 1734268137944-->


### Corollaire
Si $X$ est une solution réalisable du primal $\mathcal P$, et $V$ une solution réalisation du dual $\mathcal D$ tel que $bX = cV$ alors: #!

$X$ est une solution optimal de $\mathcal P$, et $V$ est une solution optimal de $\mathcal D$
<!--ID: 1734268137946-->



## Théorème: lien entre l'optimal primal et dual
$X^*$ est la solution optimale du problème $\mathcal P$ et $V^{*}$ la solution au dual $\mathcal D$ si et seulement si: #!

$$
\begin{cases}
V^{*}(AX^{*} - b) &= &0 \\
X^{*}(^tAV^{*} - c) &= &0
\end{cases}
$$
<!--ID: 1734268137947-->


