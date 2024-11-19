## Définition
Soit $(X, d)$ et $f: X \to \mathbb{R}$ une fonction avec $x_{0} \in X$ alors on définit les extremums de la façon suivante: #!

- f admet un maximum (resp. minimum) global en $x_{0}$ si et seulement si $\forall x \in X, f(x) \leq f(x_{0})$ (resp. $f(x) \geq f(x_{0})$)
- f admet un maximum (resp. minimum) local en $x_{0}$ si et seulement si $\exists \varepsilon > 0, \forall x \in B(x_{0}, \varepsilon), f(x) \leq f(x_{0})$ (resp. $f(x) \geq f(x_{0})$)

## Propriété sur les extremums locaux
Soit $f: \mathbb{R} \to \mathbb{R}$ et supposons que $a$ est un extremum local, alors dans ce cas: #!
$$
f'(a) = 0
$$

### Preuve
On prouve le le minimum, mais le maximum se prouve de la même façon

Supposons alors $\exists \varepsilon >0, \forall x \in B(a, \varepsilon), f(x) \geq f(a)$
Et on a $$
f(a+h) = f(a) +hf'(a) +o(h) \implies f(a+h) - f(a) = hf'(a) + o(h)
$$
Or $\forall h \in B(0, \varepsilon)$...

Si $h \geq 0$ $f'(a) + \frac{o(h)}{h} \geq 0$
et sinon $f'(a) + \frac{o(h)}{h} \leq 0$

