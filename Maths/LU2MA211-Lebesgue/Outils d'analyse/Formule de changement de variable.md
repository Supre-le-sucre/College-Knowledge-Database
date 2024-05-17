## $\mathcal C^1$-difféomorphisme
On définit $\rho: V \to U$ un $\mathcal C^1$-difféomorphisme si: #!
- $\rho$ est bijective
- les dérivées partielles de $\rho$ existent et sont continues sur $V$
- la matrice jacobienne $J_\rho$ de ses dérivées partielles est inversible (i.e son déterminant n'est pas nul)
<!--ID: 1715790676172-->


## Changement de variables
Soit $g: U \to \mathbb R$ une fonction intégrable avec $U$ un ouvert. Soit $\rho: U \to V$ un $\mathcal C^1$-difféomorphisme, alors on a que: #!
$$\int_Ug = \int_Vg \circ \rho \;|\det J_\rho|$$
<!--ID: 1715790676175-->

# Changement de variables courants
## Changement de variable en coordonnées polaires
On énonce le changement de variable en coordonnées polaires comme suit: #!

Pour effectuer un changement de variable sur $\mathbb R^2$ en coordonnées polaires, on pose $D = \mathbb R_-^* \times 0$ une demi droite de mesure nulle avec le $\mathcal C^1$-difféomorphisme: $$\rho: \mathbb R^*_+ \times ]-\pi, \pi[\to \mathbb R^2\setminus D$$$$\rho:(r, \theta) \mapsto (rcos(\theta), rsin(\theta))$$Soit alors l'intégrale de $f$ sur $\mathbb R^2$ devenant: $$\int_{\mathbb R^2}f = \int_0^{+\infty}\left(\int_{-\pi}^{\pi}f(r\cos(\theta), r\sin(\theta))d\theta\right)rdr$$Observons donc que $|\det J_\rho| = r$

## Changement de variable en coordonnées sphériques
On énonce le changement de variable en coordonnées sphériques comme suit: #!

Pour effectuer un changement de variable sur $\mathbb R^3$ en coordonnées polaires, on pose $D = \mathbb R_-^* \times 0$ une demi droite de mesure nulle avec le $\mathcal C^1$-difféomorphisme: $$\rho: \mathbb R^*_+ \times ]-\pi, \pi[\to \mathbb R^2\setminus D$$$$\rho:(r, \theta) \mapsto (rcos(\theta), rsin(\theta))$$Soit alors l'intégrale de $f$ sur $\mathbb R^2$ devenant: $$\int_{\mathbb R^2}f = \int_0^{+\infty}\left(\int_{-\pi}^{\pi}f(r\cos(\theta), r\sin(\theta))d\theta\right)rdr$$Observons donc que $|\det J_\rho| = r$
