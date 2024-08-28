# ==Définition==
On définit la transformée de Fourier de la façon suivante: #!

Soit $f: \mathbb R \to \mathbb C$ une fonction intégrable. On appelle sa transformée de Fourier, notée $\mathcal F(f)$ ou encore $\hat f$, la fonction allant de $\mathbb R \to \mathbb C$ et de la forme: $$\hat f(\xi) = \int_\mathbb R f(x)e^{-i\xi x}dx$$
<!--ID: 1715963190633-->


# Propriétés spécifiques

## Introduction de fonctions particulières
Pour une fonction $f: \mathbb R \to \mathbb C$ et un réel $a$ non nul on introduit les fonctions $e_a, \tau_af$ et $\sigma_af$ de la façon suivante: #!

- $e_a: \xi \mapsto e^{ia\xi}$
- $\tau_af: x \mapsto f(x-a)$
- $\sigma_af \mapsto f\left(\frac{x}{a}\right)$ 
<!--ID: 1715963190635-->


## La transformée rend la fonction plus lisse
On observe le résultat suivant: #!

L'application $\mathcal F: L^1(\mathbb R) \to \mathcal C^0_b$ (transformée de Fourier) est ==linéaire== et ==continue== et vérifie: $$||\hat f||_\infty \leq ||f||_1$$
## Interaction de la transformée sur $\tau_af, \sigma_af$
On observe le phénomène suivant: #!
<!--ID: 1715963190637-->


Si $f \in L^1(\mathbb R)$ et $a \in \mathbb R^*$, alors on a que
$$\widehat{\tau_af} = e_{-a}\hat f \Leftrightarrow \mathcal F(f(x-a))(\xi) = e^{-ia\xi}\hat f(\xi)$$
$$\widehat {\sigma_af} = |a|\sigma_{\frac{1}{a}}\hat f \Leftrightarrow \mathcal F\left(f\left(\frac{x}{a}\right)\right)(\xi) = |a| \widehat{f(a\xi)}$$

## Transformée de Fourier sur une dérivée
On observe le phénomène suivant: #!

Si $f \in L^1(\mathbb R) \cap \mathcal C^1(\mathbb R)$ et $f' \in L^1(\mathbb R)$ alors on a que
$$\widehat{f'}(\xi) = i\xi\hat f(\xi)$$
<!--ID: 1715963190640-->


## Dérivée d'une transformée de Fourier
On observe le phénomène suivant: #!

Si $x \mapsto (1+|x|)f(x) \in L^1(\mathbb R)$ alors $\hat f \in \mathcal C^1(\mathbb R)$ et on a que
$$(\hat f)'(\xi) = -i\,\widehat{xf}(\xi)$$
<!--ID: 1715963190642-->


## Transformée de Fourier dans l'intégrale
On observe le phénomène suivant: #!

Si $f, g \in L^1(\mathbb R)$ alors $$\int_\mathbb R \hat fg = \int_\mathbb R f \hat g$$
<!--ID: 1715963190645-->


# Lemme de Lebesgue
On observe que: #!

Si $f \in L^1(\mathbb R)$, alors on que $$\lim_{\xi \to \pm \infty}\hat f(\xi) = 0 $$
<!--ID: 1715963190648-->
