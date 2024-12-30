## Théorème de la continuité
On énonce le théorème sur la continuité des intégrales à paramètres comme suit: #!

Soit $C \subseteq \mathbb{R}^{d}$ un fermé de $\mathbb{R}^d$ muni de la convergence de la norme et $(E, \mathcal E, \mu)$ un espace mesuré. Soit une fonction $f: E \times C \to \mathbb{C}$ telle que:
- $\forall y \in C$, l'application partielle $f(\cdot, y)$ est $(\mathcal E, \mathcal B(\mathbb{C}))$-mesurable
- Pour $\mu$-presque tout $x \in E$, l'application $y \to f(x,y)$ est continue
- Il existe une fonction $g: E \to [0, \infty]$ $\mathcal E$-mesurable telle que $\int_{E}g\ d\mu< \infty$ avec $$
|f(x,y)| \leq g(x) \quad \quad \text{pour } \mu \text{-presque tout } x \in E
$$
## Théorème de la dérivabilité
On énonce le théorème sur la dérivabilité des intégrales à paramètres comme suit: #!
<!--ID: 1735577784439-->


Soit $I$ un intervalle d'extrémité distinctes de $\mathbb{R}$ et $(E, \mathcal E, \mu)$ un espace mesuré. Soit une fonction $f: E \times I \to \mathbb{C}$ telle que:
- $\forall y \in I$, l'application partielle $f(\cdot, y)$ est $(\mathcal E, \mathcal B(\mathbb{C}))$-mesurable
- $\forall y \in I$ on a que $\int_{E}|f(x,y)|\mu(dx) < \infty$
- Pour $\mu$-presque tout $x \in E$, l'application $y \to f(x,y)$ est dérivable. La dérivée est notée $\frac{\partial f}{\partial y}(x,y)$
- Il existe une fonction $g: E \to [0, \infty]$ $\mathcal E$-mesurable telle que $\int_{E}g\ d\mu< \infty$ avec $$
\left|\frac{\partial f}{\partial y}(x,y)\right| \leq g(x) \quad \quad \text{pour } \mu \text{-presque tout } x \in E
$$