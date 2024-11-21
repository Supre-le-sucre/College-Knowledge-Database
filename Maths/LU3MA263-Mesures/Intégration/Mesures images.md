## Définition
Dans un espace mesuré $(E, \mathcal E, \mu)$, $(\mathcal E, \mathcal E')$ deux espaces mesurables, avec $f: E \to E'$ une fonction $(\mathcal E, \mathcal E')$-mesurable, on définit $\nu$ comme étant la mesure image de $\mu$ par $f$ par: #!
$$
\nu(B) = \mu \left( f^{-1}(B) \right) \quad \text{ aussi noté } \quad \nu = \mu\circ f^{-1}
$$
<!--ID: 1732221918002-->




## Théorème de transfert
Dans un espace mesuré $(E, \mathcal E, \mu)$, $(\mathcal E, \mathcal E')$ deux espaces mesurables, avec $f: E \to E'$ une fonction $(\mathcal E, \mathcal E')$-mesurable avec $\nu = \mu \circ f^{-1}$ alors: #!

$$
\forall h \in \mathcal L^1_{\mathbb{C}}(E, \mathcal E, \mu), \quad \int_{E'}h(y)\nu(dy) = \int_{E} h \circ f(x) \mu(dx)
$$
<!--ID: 1732221918004-->




### Preuve
pour la preuve, vérifier l'égalité pour $\mathbb 1_{B}$ puis ensuite utiliser le lemme technique et la permutation somme intégrale sur termes positifs pour le prouver sur toutes focntions mesurables.

## Définition de la mesure de densité
Dans un espace mesuré $(E, \mathcal E, \mu)$, avec $f: E \to [0, \infty]$ une fonction $\mathcal E$-mesurable on pose la mesure de densité $f$ par rapport à $\mu$ la valeur suivante: #!

$$
\nu(A) = \int_{A} fd\mu = \int_{E}f \mathbb 1_{A}d\mu
$$
On observe alors que $\forall g: E \to \mathbb{C}$ avec $\mathcal E$-mesurable ==ou== $\nu$ intégrable que $$
\int_{E} g d\nu = \int_{E}gd\mu
$$
<!--ID: 1732221918005-->




### Preuve
Pour la deuxième assertion, on vérifie la propriété sur $\mathbb 1_{B}$ puis là encore, lemme technique puis permutation somme et intégrale pour termes $\geq 0$