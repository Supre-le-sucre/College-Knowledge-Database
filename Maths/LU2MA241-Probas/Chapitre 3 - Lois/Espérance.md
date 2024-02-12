#probas
## Définition
$X$ est une variable aléatoire discrète $X: \Omega \to \mathbb R$ avec $X(\Omega)$ un ensemble dénombrable.
$X$ admet une espérance si et seulement si #!
la somme $\sum_{x \in X(\Omega)} xp_X(x)$ est bien définie. Si c'est le cas alors cette somme est appelée espérance de $X$ et notée $\mathbb E[X]$ 
<!--ID: 1707733777453-->

## Différents cas d'espérance

### Dans $\mathbb{R}^+$ 
Soit $X(\Omega) \subset \mathbb R^+$, On pose la série $S = \sum_{x \in X(\Omega)} xp_X(x)$... Alors dans ce cas #!
La série $S$ est à termes positifs, et tends vers son supremum.
- Si la série diverge alors $\mathbb E[X] = +\infty$
- Si la série converge vers $l$, alors $\mathbb E[X]=l$ 

### Au delà de $\mathbb{R}^+$ 
Soit $X(\Omega) \not\subset \mathbb R^+$. Soit $x^+ = \max{(x, 0)}, x^- = \max{(-x, 0)}$. On pose les séries $$S_+ = \sum_{x \in X(\Omega)} x^+p_X(x)$$ $$S_- = \sum_{x \in X(\Omega)} x^-p_X(x)$$Alors on a, en considérant $S = S_+ -  S_-$ #!



