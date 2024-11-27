## Lemme de Fatou
On donne le lemme suivant: #!

Soit $f_{n}: E \to [0, \infty]$, une suite de fonctions $\mathcal E$-mesurables et positives, on a alors que $$
\int_{E}\liminf_{ n \to \infty } f_{n} d\mu \leq \liminf_{ n \to \infty } \int_{E} f_{n} d\mu 
$$
<!--ID: 1732221918017-->




### Preuve
Posons que $g_{n} = \inf_{p \geq n} f_{p}$ qui est une fonction mesurable par stabilité avec l'$\inf$
Observons aussi que $g_{n} \leq g_{n+1}$ car $g_{n}$ contient une fonction supplémentaire par rapport à $g_{n+1}$

Par le [[Convergence monotone|TCM]] on a que
$$
\int_{E}
 \left( \lim_{ n \to \infty } g_{n} \right) d\mu = \lim_{ n \to \infty } \left( \int_{E} g_{n} d\mu \right)$$
Et on a en particulier que $\lim_{ n \to \infty } g_{n} = \lim\inf_{ n \to \infty } f_{n}$
D'autre part, observons que $g_{n} \leq f_{n}$
Par propriété de l'intégrale $$
\int_{E}g_{n} d\mu \leq \int_{E}f_{n}d\mu
$$
Et par stabilité de la $\lim\inf$ on a que
$$
\lim\inf_{ n \to \infty } \left(  \int_{E}g_{n} d\mu \right) \leq \lim\inf_{ n \to \infty } \left(\int_{E}f_{n}d\mu\right)
$$
$$\lim_{ n \to \infty } \left(  \int_{E}g_{n} d\mu \right) \leq \lim\inf_{ n \to \infty } \left(\int_{E}f_{n}d\mu\right)$$
Car, en effet, $g_{n}$ converge nécessairement vers la limite inf de $f$, ce qui fait que comme elle est convergence, sa limite inf et sup est la même que sa limite

D'où l'égalité vérifiée d'après la formule de départ
$$
\int_{E}\liminf_{ n \to \infty } f_{n} d\mu = \liminf_{ n \to \infty } \int_{E} f_{n} d\mu 
$$