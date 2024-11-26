
## Définition d'une fonction de classe $\mathcal C^1$
Soit $f:\Omega \to F$ une fonction [[Différentiabilité|différentiable]] sur $\Omega$: #!

On peut définir $g: \Omega \to \mathcal L(E, F)$, $g: x \mapsto D_{f}(x)$. On dit que $f$ est $\mathcal C^1$ sur $\Omega$ si $g$ est une fonction continue.

## Théorème sur la différentiabilité de $f$ sur $\Omega$
Soit $E = \mathbb{R}^m$ et $f: \Omega \to F$: Si les hypothèses suivantes sont vérifiées #!

- Supposons que $f$ admette des dérivées partielles en tout point de $\Omega$
- Et que l'ensemble de ces dérivées partielles sont continues.

Alors $f$ est différentiable sur $\Omega$

### Preuve du théorème
Pour simplifier, on prouve le théorème sur $m=2$, mais la preuve reste la même en dimension supérieur.

Le candidat de la différentiable, obligatoire ici (voir propriétés précédentes) est
$$
D_{f}(x)(h) = \frac{\partial f}{\partial x_{1}} h_{1} + \frac{\partial f}{\partial x_{2}} h_{2}
$$
On se demande maintenant si
$$
f(x_{1} + h_{1}, x_{2} + h_{2}) = f(x_{1}, x_{2}) + D_{f}(x)(h) + o(h)
$$
Si on prouve ça, alors on aura montrer que $f$ est bien différentiable.

Calculons $f(x_{1} + h_{1}, x_{2} + h_{2})$. Par développement limité
$$
\begin{align*}
f(x_{1} + h_{1}, x_{2} + h_{2}) =& f(x_{1} + h_{1}, x_{2}) + h_{2} \frac{\partial f}{\partial x_{2}}(x_{1} + h_{1}, x_{2}) + o_{h_{1}}(h_{2})
\end{align*}
$$
Regardons $g_{h_{1}}: ]-\varepsilon, \varepsilon[ \to F$ tel que
$$
g_{h_{1}}(h_{2}) = f(x_{1} +h_{1}, x_{2} + h_{2}) - f(x_{1} + h_{1}, x_{2})
 - h_{2} \frac{\partial f}{\partial x_{2}} h_{2}(x_{1} + h_{1}, x_{2})$$
Et, on a que $\frac{\partial f}{\partial x_{2}}$ est continue sur $\Omega$ et donc uniformément continue sur $B_{f}(x, \varepsilon)$


## Corollaire
Soit $E=\mathbb{R}^m$, $f$ est de classe $\mathcal C ^ 1$ si et seulement si: #!

Les dérivées partielles de $f$ existent et sont continues.

### Preuve
$\Leftarrow$ D'après le théorème, $f$ est différentiable en tout point de $\Omega$ et $\forall x \in \Omega$, on a que 
$$D_{f}(x)(h) = \sum^m_{i=1} \frac{\partial f}{\partial x_{i}}(x)h_{i}$$
Il ne reste plus qu'à montrer que $g: \Omega \to \mathcal L(E, F)$ avec $g: x \mapsto D_{f}(x)$ est continue.

Soient $$x \in \Omega, ||D_{f}(x) - D_{f}(y)||_{\mathcal L(E, F)} = \sup_{||h|| \leq 1} || D_{f}(x)(h) - D_{f}(y)(h)||_{F}$$
Par définition.
$$
\sup_{||h|| \leq 1} || D_{f}(x)(h) - D_{f}(y)(h)||_{F} = \sup_{||h|| \leq 1} \left| \left| \sum^m_{i=1} \left(\frac{\partial f}{\partial x_{i}}(x) - \frac{\partial f}{\partial x_{i}}(x)\right)h_{i} \right|  \right| \leq C\sum_{i=1}^{m} \left| \left|\frac{\partial f}{\partial x_{i}}(x) - \frac{\partial f}{\partial x_{i}}(x)\right|  \right|
$$
Et $\left| \left|\frac{\partial f}{\partial x_{i}}(x) - \frac{\partial f}{\partial x_{i}}(x)\right|  \right| \to 0$ lorsque $x \to y$ car les dérivées partielles sont continues.
Donc $g$ est continue car lipschitzienne


