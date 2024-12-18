## Définition
Soit $(E, \mathcal E, \mu)$ un espace mesuré, avec $f: E \to \mathbb R$ une fonction $\mathcal E$-mesurable.
On dit de $f$ qu'elle est $\mu$ intégrable si: #!

$$
\int_{E}|f|d\mu < +\infty
$$
On note $\mathcal L^1_{\mathbb{R}}(E, \mathcal E, \mu)$ l'ensemble de ces fonctions
<!--ID: 1732221918008-->




## Intégrales sur fonctions à valeur sur $\mathbb{R}$
On définit l'intégrale de $f \in \mathcal L^1_{\mathbb{R}}(E, \mathcal E, \mu)$ comme suit: #!

En posant $f_{+} = \max(0, f)$ et $f_{-} = \max(0,-f)$, on donne l'égalité suivante: $$
\int_{A}fd\mu = \int_{A} f_{+} d\mu - \int_{A}f_{-}d\mu
$$
<!--ID: 1732221918010-->




## Inégalité triangulaire de l'intégrale sur $\mathcal L^1_{\mathbb{R}}(E, \mathcal E, \mu)$
On observe la propriété suivante: #!
$$
\left| \int_{E}fd\mu \right| \leq \int_{E} |f| d\mu
$$
<!--ID: 1732221918012-->




