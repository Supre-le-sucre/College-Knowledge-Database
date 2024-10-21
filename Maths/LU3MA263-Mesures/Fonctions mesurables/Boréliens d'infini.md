## Définition
On définit les tribus boréliennes sur les espaces $\overline{ \mathbb R}$, $[0, +\infty[$ et $[0, \infty]$ tel que: #!

$$\mathcal B(\overline{ \mathbb R}) = \set{B, B \cup\set{+\infty}, B\cup\set{-\infty}, B\cup\set{-\infty}\cup\set{+\infty}, B \in \mathcal B(\mathbb R)}$$
$$\mathcal B([0, +\infty[) = \set{B \cap [0, +\infty[, B \in \mathcal B(\mathbb R)}$$
$$\mathcal B([0, +\infty]) = \set{B, B \cup \set{+\infty}, \forall B \in \mathcal B([0, +\infty[)}$$
<!--ID: 1729505135342-->



## Lemme: $f$ mesurable sur le borélien
On observe que $f$ est mesurable sur le borélien de $E$ dans une telle situation: #!

Soit $f: E \to E'$ où $E'$ est égale à $\mathbb R$, $\overline{ \mathbb R}$, $[0, +\infty[$, $[0, +\infty]$. On muni $E'$ de sa tribu borélienne.
Soit $\mathcal E$ une tribu sur $E$. Alors $f$ est $(\mathcal E, \mathcal B(E))$-mesurable si et seulement si, vu comme une fonction $(\mathcal E, \mathcal B(\overline{ \mathbb R}))$-mesurable.
<!--ID: 1729505135344-->



## Lemme: Engendrement de $\mathcal B(\overline{ \mathbb R})$ 
On observe le phénomène suivant: #!

Soit $\mathcal R = \set{[-\infty, a], a \in \mathbb R}$. Alors $\sigma(\mathcal R) = \mathcal B(\overline{ \mathbb R})$
<!--ID: 1729505135346-->



### Corollaire
On peut observer une nouvelle implication pour déterminer la mesurabilité de $f$: #!

Soit $(E, \mathcal E)$ un espace mesurable et soit $f: E \to E'$ où $E'$ est égale à $\mathbb R, \overline{ \mathbb R}, [0, +\infty]$ ou $[0, +\infty]$ Alors $f$ est $(\mathcal E, \mathcal B(E'))$-mesurable si et seulement si:
$$\forall a \in \mathbb R, f^{-1}([-\infty, a]) = \set{x \in E, f(x) \leq a } \in \mathcal E$$
<!--ID: 1729505135348-->



#### Preuve
$\set{[-\infty, a] \in \mathbb R} = \mathcal R$ et $\mathcal(\mathcal R) = \mathcal B(\overline{ \mathbb R})$.
Donc $f$ vu comme une fonction $E \to \overline{ \mathbb R}$ est mesurable si et seulement si $\forall A \in \mathcal R, f^{-1}(A)  \in \mathcal E$

## Propriété: Monotonie
On peut déduire une propriété intéressante sur les propriétés monotones: #!

Soit $f: \mathbb R \to \mathbb R$ monotone, alors $f$ est $(\mathcal B(\mathbb R), \mathcal B (\mathbb R))$
<!--ID: 1729505135349-->



### Preuve
Soit $a \in \mathbb R$, $f^{-1}([-\infty, a]) = \set{x \in E, f(x) \leq a}$, comme $f$ est monotone $f^{-1}([-\infty, a])$ est un intervalle.

Et notre tribu $\sigma(\mathbb R)$ les contient tous
$$\tag*{$\blacksquare$}$$
