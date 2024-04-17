## Définition
Une [[Variable aléatoires à densité]] $X$ suit une loi uniforme sur $]a,b[$, noté $X \sim \mathcal U(]a,b[)$ si elle a pour densité: #!
$$f_X(x) = \frac{1}{b-a}\mathbb 1_{]a,b[}(x)$$ et donc on a
$$ F_X(t) = \begin{cases} 
      0 & t < a\\
      \frac{t-a}{b-a} & a \leq t \leq b \\
      1 & t > b 
   \end{cases}
$$

## Théorème de la pseudo-inverse
Soit $F: \mathbb R \to \mathbb R$ une fonction croissante, continue à droite et telle que $\lim_{x \to -\infty} F(x) = 0$ et$\lim_{x \to +\infty} F(x) = 1$ Alors on définit la fonction $\rho: ]0, 1[ \to \mathbb R$ appelée pseudo-inverse de $F$ de la façon suivante: #!
$$\rho(x) := \inf\{y \in \mathbb R\: F(y) \geq x\}$$