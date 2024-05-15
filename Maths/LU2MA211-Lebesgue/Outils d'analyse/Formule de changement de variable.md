## $\mathcal C^1$-difféomorphisme
On définit $\rho: V \to U$ un $\mathcal C^1$-difféomorphisme si: #!
- $\rho$ est bijective
- les dérivées partielles de $\rho$ existent et sont continues sur $V$
- la matrice jacobienne $J_\rho$ de ses dérivées partielles est inversible (i.e son déterminant n'est pas nul)

## Changement de variables
Soit $g: U \to \mathbb R$ une fonction intégrable avec $U$ un ouvert. Soit $\rho: U \to V$ un $\mathcal C^1$-difféomorphisme, alors on a que: #!
$$\int_Ug = \int_Vg \circ \rho \;|\det J_\rho|$$