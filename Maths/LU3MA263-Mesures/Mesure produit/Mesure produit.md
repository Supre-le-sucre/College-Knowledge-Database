# Préambule
## Définition
Soit $(E_{1}, \mathcal E_{1})$ et $(E_{2}, \mathcal E_{2})$ deux espaces mesurables. On pose alors $\mathcal P = \{ A \times B, A \in \mathcal E_{1}, B \in \mathcal E_{2} \}$ la *classe des rectangles de* $\mathcal E_{1}$ et $\mathcal E_{2}$. Il se trouve qu'il s'agit d'un [[Pi-système et classe monotone|pi-système]]. La tribu produit de $\mathcal E_{1}$ et $\mathcal E_{2}$ est alors donnée par: #!

$$
\sigma(\mathcal P) = \mathcal E_{1} \otimes \mathcal E_{2}
$$

## Définition d'une section
Pour $C \subset E_{1} \times E_{2}$ et $(x,y) \in E_{1} \times E_{2}$, on note: #!

$$
C^{1}_{x} = \{ y' \in E_{2}, (x, y') \in C\} \subset E_{2}
C^{2}_{y} = \{ x' \in E_{1}, (x', y) \in C\} \subset E_{1}
$$
$C^{1}_{x}$ est la section de $C$ en la première cordonnée, fixé à $x$

## Lemme sur les sections
On observe que pour $C \in \mathcal E_{1} \otimes \mathcal E_{2}$ alors: #!

$$
\forall(x,y) \in E_{1} \times E_{2}, C_{x}^{1} \in \mathcal E_{2} \text{ et } C_{y}^{2} \in \mathcal E_{1}
$$

# Définition

## Théorème
$(E_{1}, \mathcal E_{1}, \mu_{1})$ et $(E_{2}, \mathcal E_{2}, \mu_{2})$ deux espaces mesurés avec $\mu_{1}$ et $\mu_{2}$, $\sigma$-finies alors observons les propriétés suivantes: #!

1) $\forall C \in \mathcal E_{1} \otimes \mathcal E_{2}$ $$
x \mapsto \mu_{2}(C_{x}^{1}) \text{ et } y \mapsto \mu_{1}(C_{y}^{2})
$$Sont respectivement $\mathcal E_{1}$ et $\mathcal E_{2}$ mesurables.
2) 