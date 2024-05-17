# ==Définition==
On définit la transformée de Fourier de la façon suivante: #!

Soit $f: \mathbb R \to \mathbb C$ une fonction intégrable. On appelle sa transformée de Fourier, notée $\mathcal F(f)$ ou encore $\hat f$, la fonction allant de $\mathbb R \to \mathbb C$ et de la forme: $$\hat f(\xi) = \int_\mathbb R f(x)e^{-i\xi x}dx$$

# Propriétés spécifiques

## Introduction de fonctions particulières
Pour une fonction $f: \mathbb R \to \mathbb C$ et un réel $a$ non nul on introduit les fonctions $e_a, \tau_af$ et $\sigma_af$ de la façon suivante: #!

- $e_a: \xi \mapsto e^{ia\xi}$
- $\tau_af: x \mapsto f(x-a)$
- $\sigma_af \mapsto f\left(\frac{x}{a}\right)$ 

## La transformée rend la fonction plus lisse
On observe le résultat suivant: #!

L'application $\mathcal F: L^1(\mathbb R) \to \mathcal C^0_b$ (transformée de Fourier) est ==linéaire== et ==continue== et vérifie: $$||\hat f||_\infty \leq ||f||_1$$
## Interaction de la transformée sur $\tau_af, \sigma_af$
On observe le phénomène suivant: #!

Si $f \in L^1(\mathbb R)$ et $a \in \mathbb R^*$, alors on a que
$$\widehat{\tau_af} = e_{-a}\hat f \Leftrightarrow \mathcal F(f(x-a))(\xi) = e^{-ia\xi}\hat f(\xi)$$
$$\widehat {\sigma_af}$$