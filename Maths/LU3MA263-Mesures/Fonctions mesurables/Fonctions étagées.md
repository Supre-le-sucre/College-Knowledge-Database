## Mesurabilité de $\mathbb 1$
La fonction indicatrice est mesurable de $A \subset E$ est $(\mathcal E, \mathcal E)$-mesurable si et seulement si: #!
$$A \in \mathcal E$$
<!--ID: 1732147465911-->


## Définition
Une fonction $s: E \to \mathbb{R}$ $\mathcal E$-mesurable est dite étagée si et seulement si: #!

Elle peut s'écrire comme une combinaison linéaire ==finie== d'indicatrice i.e
$$
s = \sum_{k=1}^{n} c_{k}\mathbb 1_{A_{k}}
$$**Remarque**: Une fonction étagée n'admet pas une seule et unique décomposition $$
s = \mathbb 1_{E} = \mathbb 1_{A} + \mathbb 1_{A^c}
$$
## Propriété convergence vers une fonction mesurable
On observe la propriété suivante: #!
<!--ID: 1732147465914-->


Soit $f: E \to [0, \infty]$ une fonction $\mathcal E$ mesurable.
Alors il existe une suite $s_{n}: E \to [0, \infty]$ de fonction étagée $\mathcal E$ mesurable telle que $s_{n} \leq s_{{n+1}}$ et $$
\lim_{ n \to \infty } s_{n}=f \quad \quad \text{ et } \quad \quad s_{n} \leq f
$$
# Lemme technique
On observe la propriété suivante qui nous sera bien utile pour la suite: #!

Soit $(E, \mathcal E)$ un espace mesurable avec $f: E \to [0,\infty]$ mesurable. Alors il existe $B_{n} \in \mathcal E$ et $c_{n} \in ]0, \infty[$ tel que
$$
f = \sum_{n\in \mathbb{N}} c_{n} \mathbb 1_{B_{n}}
$$
<!--ID: 1732147465916-->


### Preuve
Soit $s_{n}$ une suite de fonctions mesurable étagée positive avec $s_{n} \leq s_{n+1}$ et tel que $\lim_{ n \to \infty } s_n = f$

On pose $t_{0} = s_{0}$ et $t_{n} = s_{n} - s_{n-1}$
Les fonctions $t_{n}$ sont aussi étagée positive.
Ainsi $\exists N_{n}$ tel que $\exists (c_{1}^n, \dots, c_{N_{n}}^n) > 0$ et $\exists (A_{1}^n, \dots, A_{N_{n}}^n)$ avec $$
t_{n} = \sum_{k=1}^{N_{n}}c_{k}^n\mathbb 1_{A_{k}^n} 
$$
Et en particulier, on observe que $\sum_{k=0}^{n}t_{k }=s_{n}$
D'où finalement $$
\sum_{k\in \mathbb{N}} t_{k} = \lim_{ n \to \infty } \sum_{k=0}^{n}t_{k} = \lim_{ n \to \infty } s_{n} =f
$$
Avec donc
$$
f = \sum_{n\in\mathbb{N}}\sum_{k=1}^{N_{n}}c_{k}^n \mathbb 1_{A_{k}^n}  = \sum_{n \in \mathbb{N}}c_{n} \mathbb 1_{B_{n}}
$$
Par réorganisation des indices (possibles car somme à termes positif)
