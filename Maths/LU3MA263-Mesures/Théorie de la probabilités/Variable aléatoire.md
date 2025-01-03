## Définition
On définit une variable aléatoire dans un espace mesurable $(E, \mathcal E)$ et l'espace probabilisé $(\Omega, \mathcal F, \mathbb{P})$ comme étant: #!

Une fonction $X: \Omega \to E$ étant $(\mathcal F, \mathcal E)$-mesurable.
On notera que souvent que: $$
\{ X \in C \} = X^{-1}(C)
$$
Une variable aléatoire est qualifiée de réelle si son espace d'arrivé est $(\mathbb{R}, \mathcal B(\mathbb{R}))$
<!--ID: 1735577943257-->



## Espérance
Soit $X: \Omega \to [0, \infty]$ une variable aléatoire, on définit son espérance comme suit: #!

$$
\mathbb E(X) = \int_{\Omega} X d\mathbb P
$$
Pour $X: \Omega \to \mathbb{C}$, l'espérance existe si $\mathbb E(|X|) < \infty$
<!--ID: 1735577943258-->



## Loi d'une variable aléatoire
Soit $(E, \mathcal E)$ un espace mesurable et soit $X: \Omega \to E$ une variable aléatoire. La loi de $X$ est alors définie comme étant: #!

La [[Mesures images|mesure image]] de $\mathbb{P}$ par $X$ que l'on notera $\mu_{X}$. Ainsi donc on a que $\mu_{X} = \mathcal E \to [0, 1]$ définie $\forall C \in \mathcal E$ avec $$
\mu_{X}(C) = \mathbb{P}(X^{-1}(C)) = \mathbb{P}(\{ X \in C \})
$$
Observons que $\mu_{X}$ est alors une mesure de probabilité.
<!--ID: 1735577943260-->



## Formule de transfert
Soit $X$ une variable aléatoire de $\Omega \to E$ et $\mu_{X}$ sa loi: #!

Alors $\forall h: E \to [0, \infty]$, $\mathcal E$-mesurable on a alors $$
\int_{\Omega}h(X)d\mathbb P = \mathbb{E}(h(X)) = \int_{E}h d\mu_{X}
$$
De même si $h$ est à valeur dans $\mathbb{C}$ et $\mathbb{E}(|h(X)|) < \infty$
<!--ID: 1735577943261-->




# Cas discret

## Définition
Soit $(E, \mathcal E)$ un espace mesurable tel que $\forall y \in E$ et $\{  y \} \in \mathcal E$. On dit que $X: \Omega \to E$ est discrète si: #!

L'ensemble $X(\Omega)$ est dénombrable
<!--ID: 1735577943263-->



## Loi d'une variable aléatoire discrète
La loi de $X$ est donné par: #!

$$
\mu_{X} = \sum_{y \in X(\Omega)}a_{y}\delta_{y} \text{ où } a_{y} = \mathbb{P}(X =y)
$$
<!--ID: 1735577943264-->



## Combinaison de fonction avec une variable aléatoire
Dans le cas d'une variable aléatoire discrètes on a que: #!

Pour toute fonction $f: E \to \mathbb{R}$ est $\mathcal E$-mesurable **positive ou bornée**. Alors $f(X)$ est aussi une variable aléatoire discrète, d'où $$
\mathbb{E}(f(X)) = \sum_{y \in X(\Omega)}f(y)\mathbb{P}(X=y)
$$
<!--ID: 1735577943266-->

