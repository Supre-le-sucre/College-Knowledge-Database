#probas

## Inégalité de Markov
Soit $X$ une [[Variable aléatoire réelle]] à valeurs positives. Alors on a: #!
$$\forall \epsilon > 0, \mathbb P(X \geq \epsilon) \leq \frac{\mathbb E(X)}{\epsilon}$$
<!--ID: 1713305360708-->


## Inégalité de Bienaymé-Tchebychev
Soit $X$ une [[Variable aléatoire réelle]] admettant un [[Moments]] d'ordre 2. Alors on a: #!
$$\mathbb P(|X - \mathbb E(X)| \geq \epsilon) \leq \frac{Var(x)}{\epsilon^2}$$
<!--ID: 1713305360718-->


## Inégalité de Cauchy-Schwarz
Soient $X$ et $Y$ des [[Variable aléatoire réelle]] admettant un [[Moments]] d'ordre 2. Alors on a: #!
Pour le produit $XY$, s'il admet une espérance fini, l'inégalité: $$|\mathbb E(XY)| \leq \sqrt{\mathbb E(X^2)\mathbb E(Y^2)}$$
Remarquons donc que:
$$|\mathbb E(\mathbb 1_A\mathbb 1_B)| \leq \mathbb E(\mathbb 1_A^2)\mathbb E(\mathbb 1_B^2) \Leftrightarrow \mathbb P(A \cap B) \leq \sqrt{\mathbb P(A)\mathbb P(B)}$$
<!--ID: 1713305360722-->
