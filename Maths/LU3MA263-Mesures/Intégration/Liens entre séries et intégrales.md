## Propriété: liens entre intégrales et séries focnctions positives
Soit $(f(n))_{n \in \mathbb{N}}$ une suite à valeurs dans $[0, \infty]$. On considère ici l'espace mesurable $(\mathbb{N}, \mathcal P(\mathbb{N}), \#)$ où $\#$ est la mesure de comptage, alors on a que: #!

On pose $f = (f(n))_{{n \in \mathbb{N}}}$ à valeurs dans $[0, \infty]$, alors $$
\int_{\mathbb{N}}fd\# = \sum_{n \in \mathbb{N}}f(n)
$$Une quantité qui est possiblement

### Preuve
Observons que l'on peut réécrire la fonction $f$ comme étant
$$
f= \sum_{p \in \mathbb{N}} f(p) \mathbb 1_{\{ p \}}
$$
Avec cette réécriture, en posant l'intégrale et utilisant l'inversion somme intégrale pour des fonctions positives on a que: 
$$
\begin{align*}
\int_{\mathbb{N}} f d\#= & \int_{\mathbb{N}}\left(\sum_{n \in \mathbb{N}} f(n) \mathbb 1_{ n}\right) d\# \\
= & \sum_{n \in \mathbb{N}}\int_{\mathbb{N}}\left( f(n) \mathbb 1_{ n}\right) d\# \\
= &  \sum_{n \in \mathbb{N}}  f(n) \int_{\mathbb{N}} \mathbb 1 _{n} d\# \\
= & \sum_{n \in \mathbb{N}}  f(n) \times \#(\{ n \}) \\
= & \sum_{n \in \mathbb{N}}  f(n) 
\end{align*}
$$

## Propriété: liens entre intégrales et séries fonctions dans $\mathbb{C}$
Soit $(f(n))_{n \in \mathbb{N}}$ une suite à valeurs dans $\mathbb{C}$. On considère ici l'espace mesurable $(\mathbb{N}, \mathcal P(\mathbb{N}), \#)$ où $\#$ est la mesure de comptage, les assertions suivantes sont vérifiées: #!

D'après la propriété précédente: $$
\sum_{n \in \mathbb{N}} |f(n)| = \int_{E}|f|d\#
$$
Donc, la série des $(f(n))_{n \in \mathbb{N}}$ est absolument convergente ==si et seulement si== $f$ est $\#$-intégrable.
De plus si c'est le cas, on pose l'égalité
$$
\sum_{n \in \mathbb{N}} |f(n)| = \int_{E}|f|d\#
$$

## Corollaire sur les séries
Soit $(a_{n})_{n \in \mathbb{N}}$ et pour tout $p \in \mathbb{N}$, soient $(a_{n}^{(p)})$