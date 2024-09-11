
## Théorème du changement de variable en dimension un
On énonce le changement de variable comme suit: #!

Soit $I$ un segment et $f: I \to \mathbb C$ continue avec $\rho: [a,b] \to I$ de classe $\mathcal C^1$ alors
$$\int_{\rho(a)}^{\rho(b)}f(x)dx = \int_a^bf(\rho(t))\rho'(t)dt$$
<!--ID: 1715959200360-->



## $\mathcal C^1$-difféomorphisme
On définit $\rho: V \to U$ un $\mathcal C^1$-difféomorphisme si: #!
- $\rho$ est bijective
- les dérivées partielles de $\rho$ existent et sont continues sur $V$
- la matrice jacobienne $J_\rho$ de ses dérivées partielles est inversible (i.e son déterminant n'est pas nul)
<!--ID: 1715790676172-->


## Changement de variables
La formule général du changement de variable peut s'énoncer comme suit: #!

Soit $f: V \to \mathbb R$ une fonction intégrable avec $V$ un ouvert. Soit $\rho: U \to V$ avec $U$ un ouvert et $\rho$ un $\mathcal C^1$-difféomorphisme. 
On a que $f$ est intégrable sur $V$ si et seulement si $f \circ \rho$ l'est sur $U$. 
Ce qui donne le changement de variable suivant: 
$$\int_Vf(x)dx = \int_U f(\rho(y)) \;|\det J_\rho(y)|dy$$
<!--ID: 1715959200362-->



# Changement de variables courants

## Changement de variable affine
On énonce le changement de variables affine comme suit: #!

Si $f: \mathbb R^d \mapsto \mathbb C$ est intégrable, en posant: $\lambda \in \mathbb R$ et $a\in\mathbb R^d$ avec $x = \lambda y + a$ on obtient le changement de variable suivant: $$\int_{\mathbb R^d} f(x)dx = |\lambda^d|\int_{\mathbb R^d}f(\lambda y +a)dy$$
<!--ID: 1715959200365-->


## Changement de variables en coordonnées polaires
On énonce le changement de variable en coordonnées polaires comme suit: #!

Pour effectuer un changement de variable sur $\mathbb R^2$ en coordonnées polaires, on pose $D = \mathbb R_-^* \times 0$ une demi droite de mesure nulle avec le $\mathcal C^1$-difféomorphisme: $$\rho: \mathbb R^*_+ \times ]-\pi, \pi[\to \mathbb R^2\setminus D$$$$\rho:(r, \theta) \mapsto (r\cos(\theta), r\sin(\theta))$$Soit alors l'intégrale de $f$ sur $\mathbb R^2$ devenant: $$\int_{\mathbb R^2}f = \int_0^{+\infty}\left(\int_{-\pi}^{\pi}f(r\cos(\theta), r\sin(\theta))d\theta\right)rdr$$Observons donc que $|\det J_\rho| = r$
<!--ID: 1715959200366-->


## Changement de variables en coordonnées sphériques
On énonce le changement de variable en coordonnées sphériques comme suit: #!

Pour effectuer un changement de variable sur $\mathbb R^3$ en coordonnées sphériques, on pose le $\mathcal C^1$-difféomorphisme: $$\rho: \mathbb R^*_+ \times ]-\pi, \pi[ \times ]0, \pi[ \to \mathbb R^3$$$$\rho:(r, \theta, \phi) \mapsto (r\cos(\theta)\sin(\phi), r\sin(\theta)\sin(\phi), r\cos(\phi))$$Soit alors l'intégrale de $f$ sur $\mathbb R^3$ devenant: $$\int_{\mathbb R^3}f = \int_{\mathbb R_+^* \times]-\pi, \pi[ \times ]0, \pi[}f\left(r\cos(\theta)\sin(\phi), r\sin(\theta)\sin(\phi), r\cos(\phi)) r^2\sin(\phi\right)drd\theta d\phi $$Observons donc que $|\det J_\rho| = r^2\sin(\phi)$
<!--ID: 1715959200368-->


