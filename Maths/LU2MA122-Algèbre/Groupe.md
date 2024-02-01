#algebre 
## Définition
Soit $*$ une [[Loi de composition interne (LCI)|LCI]] sur $E$. On qualifie le [[Monoïde]] $(E, *)$ de groupe lorsqu'il vérifie la propriété suivante (existence d'un inverse):
$$ \forall x \in E, \exists y \in E, x*y=y*x=e $$
Avec $e$ l'élément neutre du monoïde. On parle de groupe abélien si $(E, *)$ est un [[Monoïde]] abélien.

*Exemple:* $(\mathbb{Z}, +)$ est un groupe abélien.

## Unicité de l'élément neutre et de l'inverse

### Lemme 
Soit $(E, *)$ un ensemble avec une [[Loi de composition interne (LCI)]], si elle admet un élément neutre (cf. [[Monoïde]]), alors celui-ci est unique.
Si de plus $(E, *)$ est un [[Groupe]], alors il y a unicité de l'inverse.

#### Démonstration
Soit $(E, *)$ un tel ensemble et $e$ et $e'$ deux éléments neutres.
Par définition de l'élément neutre: $e * e' = e$ et $e*e' = e'$, d'où $e=e'$

Supposons que $(E, *)$ est une groupe.
Soit $y$ et $y'$ les inverses de l'élément $x$ dans un tel groupe.

Dans ce cas, observons que $y = y*(x*y')$ car $(x*y') = e$ 
Soit alors par commutativité, sachant aussi que $(y*x) =e$
$$y = y * (x*y') = (y*x)*y' = y'$$
$$\tag*{$\blacksquare$}$$
#### Corollaire
Il est donc possible d'écrire par ce lemme: $x^{-1}$ l'inverse de $x$.
Aussi, observons que $(x*y)^{-1} = y^{-1} * x^{-1}$

En effet, $$(x*y)*(y^{-1}* x^{-1}) = x * (y * y^{-1})*x^{-1} = x * x^{-1} = e $$$$\tag*{$\blacksquare$}$$
## Erreurs courantes

### Distribution de la puissance
$$(xy)^n \not = x^n * y^n \text{ en général}$$
Il est nécessaire d'avoir la <b><u>commutativité</b></u>
*Exemple:* Les matrices ne respecte effectivement pas cette distribution