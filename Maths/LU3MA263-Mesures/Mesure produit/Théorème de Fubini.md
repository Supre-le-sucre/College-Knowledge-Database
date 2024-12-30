## Lemme
Soit $(E_{1}, \mathcal E_{1})$ et $(E_{2}, \mathcal E_{2})$ deux espaces mesurables et $f: E_{1} \times E_{2} \to \overline{\mathbb{R}}$ (ou $\mathbb{C}$) une fonction $(\mathcal E_{1} \otimes \mathcal E_{2})$-mesurable. Alors observons que: #!

$$
\forall x_{0} \in E_{1}, y \mapsto f(x_{0}, y) \text{ est } \mathcal E_{2}\text{-mesurable, et vice-versa}
$$
<!--ID: 1735577784382-->


## Théorème de Fubini positif
Soit $(E_{1}, \mathcal E_{1}, \mu_{1})$ et $(E_{2}, \mathcal E_{2}, \mu_{2})$ deux espaces mesurés avec $\mu_{1}$ et $\mu_{2}$, $\sigma$-finies. Soit $f: E_{1} \times E_{2} \to \overline{\mathbb{R}}$ (ou $\mathbb{C}$) une fonction $(\mathcal E_{1} \otimes \mathcal E_{2})$-mesurable alors on a que: #!

1) La fonction ci-dessous est $\mathcal E_{2}$-mesurable et vice-versa
$$
E_{2} \to [0, \infty] \quad y \mapsto \int_{E_{1}}f(x,y)\mu_{1}(dx)
$$
2) On a l'égalité suivante
$$
\int_{E_{1} \times E_{2}} f d(\mu_{1} \otimes \mu_{2}) = \int_{E_{1}}\left( \int_{E_{2}} f(x,y)\mu_{2}(dy)\right)\mu_{1}(dx) = \int_{E_{2}}\left( \int_{E_{1}} f(x,y)\mu_{1}(dx)\right)\mu_{2}(dy)
$$
<!--ID: 1735577784384-->


## Théorème de Fubini général
Soit $(E_{1}, \mathcal E_{1}, \mu_{1})$ et $(E_{2}, \mathcal E_{2}, \mu_{2})$ deux espaces mesurés avec $\mu_{1}$ et $\mu_{2}$, $\sigma$-finies. Soit $f: E_{1} \times E_{2} \to \overline{\mathbb{R}}$ (ou $\mathbb{C}$) une fonction $(\mathcal E_{1} \otimes \mathcal E_{2})$-mesurable ==telle que== $\int_{E_{1} \times E_{2}} f d(\mu_{1} \otimes \mu_{2}) < \infty$ alors on a que: #!

1) Pour $\mu_{2}$-presque tout $y$, l'application partielle $f(\cdot, y)$ est $\mu_{1}$-intégrable et vice-versa
2) Pour $\mu_{2}$-presque tout $y$, l'intégrale $\int_{E_{1}}f(x,y)\mu_{1}(dx)$ est bien définie, et la fonction $h$ définie pour $\mu_{2}$-presque tout $y$ telle que $$
h(y) = \int_{E_{1}}f(x,y) \mu_{1}(dx)
$$ est telle que $\int_{E_{2}} |h| d\mu_{2}< \infty$ et $\mathcal E_{2}$-mesurable. Et vice-versa
3) On a l'égalité suivante $$
\int_{E_{1} \times E_{2}} f d(\mu_{1} \otimes \mu_{2}) = \int_{E_{1}}\left( \int_{E_{2}} f(x,y)\mu_{2}(dy)\right)\mu_{1}(dx) = \int_{E_{2}}\left( \int_{E_{1}} f(x,y)\mu_{1}(dx)\right)\mu_{2}(dy)
$$
<!--ID: 1735577784386-->
