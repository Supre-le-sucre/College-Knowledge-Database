## ==Définition==
On définit le produit de convolution entre deux fonctions de la façon suivante: #!

Soient $f,g: \mathbb R \to \mathbb C$ deux fonctions mesurables. Le produit de convolution de $f$ par $g$ est l'application $f * g: \mathbb R \to \mathbb C$ définie (lorsque cela a un sens) par:
$$(f*g)(x) = \int_\mathbb Rf(x-y)g(y)dy$$
Par changement de variable $y' = x-y$, observons que le produit de convolution est commutatif, soit $f*g = g*f$
<!--ID: 1714516791376-->



## Propriété indispensable sur l'existence
On peut dire que le produit de convolution existe forcément dans les cas suivants: #!

- Si $f,g \in L^1(\mathbb R)$  $f*g$ est bien définie presque partout, avec en particulier $f*g \in L^1(\mathbb R)$.
- Si $f \in L^1(\mathbb R)$ et $g \in L^2(\mathbb R)$, alors $f*g$ est bien définie presque partout, avec en particulier $f*g \in L^2(\mathbb R)$
- Si $f \in L^1(\mathbb R)$ et $g \in \mathcal C^0_b$ alors $f*g$ est bien définie, avec en particulier $f*g \in \mathcal C^0_b$
- Si $f,g$ deux [[Fonctions à support compact]], alors $f*g$ est défini et également à support compact
<!--ID: 1714516791377-->



## Inégalités triangulaires de la convolution
On peut définir les inégalité suivante: #!

Si $f,g \in L^1(\mathbb R)$, alors $f*g \in L^1(\mathbb R)$ et on a donc: $$||f*g||_1 \leq ||f||_1||g||_1$$ De la même façon Si $f \in L^1(\mathbb R)$ et $g \in L^2(\mathbb R)$ alors $f*g \in L^2(\mathbb R)$ et on a donc:
$$||f*g||_2 \leq ||f||_1||g||_2$$
Si $f \in L^1(\mathbb R)$ et $g \in \mathcal C^0_b$ alors $f*g \in \mathcal C^0_b$ et on a donc:
$$||f*g||_\infty \leq ||f||_1||g||_\infty$$
<!--ID: 1714516791379-->


## Dérivation sur convolution
On observe le phénomène suivant: #!

Si $f \in L^1(\mathbb R)$ et $g \in \mathcal C^1$ de dérivée borné, alors $f*g \in \mathcal C^1(\mathbb R)$ a aussi une dérivée bornée, avec en particulier: $$(f *g)' = f*(g')$$ et on observe $$||(f*g)'||_\infty \leq ||f||_1||g'||_\infty$$
<!--ID: 1714516791380-->

