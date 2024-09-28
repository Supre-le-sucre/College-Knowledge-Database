## Notations
- $a \wedge b = \min(a,b)$
- $a \vee b = \max(a,b)$
- $(a)_+ = \min(0, a)$
- $(a)_- = \max(-a, 0)$
- $\lim\inf a_n = \sup_{n \in \mathbb N} \inf_{p \geq n} a_p$
- $\lim\sup a_n = \inf_{n \in \mathbb N} \sup_{p \geq n} a_p$

## Définitions
Une suite de fonction $(f_n)_{n \in \mathbb N}$ converge simplement si et seulement si: #!

$$\forall x \in E, \lim_{n \to +\infty} f_n(x) = f(x)$$
Ainsi $f_n \xrightarrow[]{c.v.s} f \Leftrightarrow \lim \inf f_n = \lim \sup f_n = f$
<!--ID: 1727559283070-->


## Propriété min, max, inf et sup sur la mesurabilité
Soit $(E, \mathcal E)$ un espace mesurable $f, g, f_n$ des fonctions $E \to [-\infty, +\infty]$ $\mathcal E$-mesurables alors: #!

i) $\forall c \in \mathbb R$, la fonction constante en $c$ est $\mathcal E$-mesurable et $cf$ l'est aussi
ii) $f \wedge g, f \vee g, (f)_-, (f)_+$ et $|f|$ sont $\mathcal E$-mesurable
iii) $\inf_{n \in \mathbb N} f_n,\sup_{n \in \mathbb N} f_n, \lim\inf a_n, \lim\sup a_n$ sont $\mathcal E$-mesurable
iv) Si $f = \lim_{n \to +\infty} f_n$ pour tout $x$, alors $f$ est mesurable $\mathcal E$-mesurable
<!--ID: 1727559283072-->


