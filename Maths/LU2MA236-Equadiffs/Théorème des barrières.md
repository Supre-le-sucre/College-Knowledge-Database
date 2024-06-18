# Sur et sous-solutions
On définit une sur-solution et une sous-solution de la façon suivante: #!

Soit $f: I \times U \to \mathbb R$ où $I$ un intervalle ouvert de $\mathbb R$ et $U$ un ouvert de $\mathbb R$
On appelle sur-solution stricte de l'EDO $x' = f(t,x)$, une fonction $u$ dérivable telle que: $$\forall t \in ]\alpha, \beta[\;\; u'(t) > f(t, u(t))$$D'où, une sous-solution stricte, une fonction $u$ dérivable telle que: $$\forall t \in ]\alpha, \beta[\;\; u'(t) < f(t, u(t))$$

# Lemme du croisement
On donne le lemme suivant: #!

Soit $u: ]\alpha, \beta[ \to \mathbb R$ une sur-solution stricte et $x:]\alpha, \beta[ \to \mathbb R$ une solution de l'équation.
Soit $b \in ]\alpha, \beta[$ tel que $u(b) = x(b)$ alors:
$$\exists \epsilon > 0 \; \begin{cases} \forall t \in ]b- \epsilon, b[ & x(t) > u(t) \\ \forall t \in ]b, b+\epsilon[ & x(t) < u(t) \end{cases}$$Evidemment, ce lemme est aussi valable pour une sous-solution en inversant les inégalités.