
## Définition
On définit la convergence en $(\mathbb P$-)probabilité de la façon suivante: #!

Soient $(X_n)_{n \in \mathbb N}$ et $X$ des variables aléatoires réelles, toutes définies sur le même espace probabilisé. On dit que la suite $(X_n)_{n \in \mathbb N}$ converge en $(\mathbb P$-)probabilité vers $X$, noté $(X_n) \to^\mathbb P X$ si pour tout $\epsilon > 0$ on a que:
$$\lim_{n \to +\infty} \mathbb P(|X_n - X| \geq \epsilon) = 0$$
De façon équivalente on dit que $(X_n)_{n \in \mathbb N}$ converge en $(\mathbb P$-)probabilité vers $+ \infty$ (resp. $-\infty$) si pour tout $A > 0$ on a que
$$\lim_{n \to +\infty} \mathbb P(X_n \leq A) = 0 \text{ (resp.}\lim_{n \to +\infty} \mathbb P(X_n \geq -A) = 0)$$
<!--ID: 1715790676112-->


## Continuité discrète par convergence en probabilité
On observe le résultat suivant: #!

Si $(X_n)_{n \in \mathbb N} \to^\mathbb P X$ et $(Y_n)_{n \in \mathbb N} \to^\mathbb P Y$ (où toutes les variables aléatoires sont définies dans le même espace probabilisé). Alors pour toute fonction continue $f: \mathbb R^2 \to \mathbb R$ on a que:
$$(f(X_n, Y_n))_{n \in \mathbb N} \to^\mathbb P f(X, Y)$$
En particulier, observons que ceci implique que
- pour toute fonction continue $g: \mathbb R \to \mathbb R$ on a que $(g(X_n))_{n \in \mathbb N} \to^\mathbb Pg(X)$
- on a que $(X_n +Y_n)_{n \in \mathbb N} \to^\mathbb P X +Y$
- ou encore que $(X_nY_n)_{n \in \mathbb N} \to^\mathbb P XY$
<!--ID: 1715790676117-->
