
## Inégalité de Jensen
Soit $I$ un intervalle de $\mathbb{R}$ et soit $\phi: I \to \mathbb{R}$ une fonction convexe. Soit $X: \Omega \to I$ une [[Variable aléatoire]] tel que $\mathbb{E}(|X|) < \infty$ et $\mathbb{E}(\phi(X)) < \infty$. Alors: #!

$$
\mathbb{E}(X) \in I \text{ et } \phi(\mathbb{E}(X)) \leq \mathbb{E}(\phi(X))
$$


### Corollaire
Soit $p, q \in \mathbb{N}^*$ tel que $p < q$, l'inégalité de Jensen permet d'affirmer le fait suivant: #!

Si $X$ admet un [[Moments|moment]] d'ordre $q$ alors il admet aussi un moment d'ordre $p$. i.e $$
\mathbb{E}(|X|^{q}) < \infty \text{ et } \mathbb{E}(|X| ^p ) < \infty
$$

## Inégalité de Holder
Soit $p \geq 1$ et soit $q \geq 1$ tel que $\frac{1}{p} + \frac{1}{q} = 1$ alors on a: #!

$$
\forall X, Y \text{ variables aléatoires } \mathbb{E}(|XY|) \leq \mathbb{E}(|X|^p)^{\frac{1}{p}}\mathbb{E}(|X|^q)^{\frac{1}{q}}
$$

## Inégalité de Minkowski
$\forall X, Y$ variables aléatoires et pour $p > 2$ on a que: #!

$$
(\mathbb{E}((|X|+|Y|)^p)^{\frac{1}{p}} \leq \mathbb{E}(|X|^p)^{\frac{1}{p}} + \mathbb{E}(|Y|^p)^{\frac{1}{p}}
$$

## Inégalité de Markov
Soit $\phi: \mathbb{R}_{+} \to \mathbb{R}_{+}$ une fonction croissante. Alors pour tout $X$ une [[Variable aléatoire]] positive, on a que

$$
\mathbb{P}(X \geq a) \leq \frac{1}{\phi(a)}\mathbb{E}(\phi(X))
$$

### Preuve
Observons que
$$
\mathbb 1_{X \geq a} \leq \frac{\phi(X)}{\phi(a)}
$$
En effet, soit $\omega$ tel que $X(\omega) < a$ alors $\mathbb{1}_{X \geq a} = 0$ et $\frac{\phi(X)}{\phi(a)} \geq 0$
Et lorsque $X(\omega) \geq a$ alors $\mathbb{1}_{X \geq a} = 0$ et $\frac{\phi(X)}{\phi(a)} \leq 1$ car $\phi$ est croissante

On intègre ensuite sur $\Omega$
$$
\begin{align}
\mathbb 1_{X \geq a} & \leq \frac{\phi(X)}{\phi(a)}  \\
\int_{\Omega} 1_{X \geq a} & \leq \int_{\Omega}\frac{\phi(X)}{\phi(a)} \\
\mathbb{P}(X \geq a) &\leq \frac{\mathbb{E}(\phi(X))}{\phi(a)}
\end{align}
$$



## Inégalité de Bienaymé-Tchebychev
Soit $X$ une [[Variable aléatoire]] tel que $\mathbb{E}(X^{2})< \infty$, alors on a que: #!

$$
\mathbb{P}(|X - \mathbb{E}(X)| \geq a) \leq \frac{Var(X)}{a^{2}}
$$
Où $Var(X)$ est la [[Maths/LU3MA263-Mesures/Théorie de la probabilités/Espérance#V0ariance|variance]] de $X$