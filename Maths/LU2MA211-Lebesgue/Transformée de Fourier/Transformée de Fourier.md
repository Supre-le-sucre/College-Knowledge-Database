# ==Définition==
On définit la transformée de Fourier de la façon suivante: #!

Soit $f: \mathbb R \to \mathbb C$ une fonction intégrable. On appelle sa transformée de Fourier, notée $\mathcal F(f)$ ou encore $\hat f$, la fonction allant de $\mathbb R \to \mathbb C$ et de la forme: $$\hat f(\xi) = \int_\mathbb R f(x)e^{-i\xi x}dx$$

# Propriétés spécifiques

## Introduction de fonctions particulières
Pour une fonction $f: \mathbb R \to \mathbb C$ et un réel $a$ non nul on introduit les fonctions $e_a, \tau_af$ et $\sigma_af$ de la façon suivante: #!

- $e_a: \xi \mapsto e^{ia\xi}$
- $\tau_af: x \mapsto f(x-a)$
- $\sigma_af \mapsto f\left(\frac{x}{a}\right)$ 