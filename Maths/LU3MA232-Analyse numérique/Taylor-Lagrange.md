## Théorème de Taylor-Lagrange
On énonce le théorème suivant: #!

Soit $n \geq 1$. Si une fonction $f$, ayant pour domaine de définition $D_f$, est de classe $\mathcal C^n$ sur un voisinage d'un point $a \in \mathbb R$ et à valeur dans $\mathbb R$, alors pour tout $h$ tel que $[a, a+h] \subseteq D_f$ on a que $$\left|f(a+h) - \left(f(a) + hf'(a) + \frac{h^2f''(a)}{2} + \cdots + \frac{h^{n-1}f^{(n-1)(a)}}{(n-1)!}\right)\right| \leq \frac{|h|^n}{n!} \sup_{t \in [a, a+h]}\left|f^{(n)}(t)\right|$$

## Théorème des accroissements finis
On énonce le théorème suivant: #!

$$\left|f(a+h) - f(a)\right| \leq |h|^n \sup_{t \in [a, a+h]}\left|f'(t)\right|$$Observons qu'il s'agit du théorème de Taylor-Lagrange avec $n= 1$
