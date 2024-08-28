
## Polynômes de Bernstein
A toute fonction $f : [0,1] \to \mathbb R$ on associe la suite suivante de polynômes, appelés *"polynômes de Bernstein* de $f$: #!

$$B_n^f(x) := \sum_{k=0}^n\binom{n}{k}f\left(\frac{k}{n}\right)x^k(1-x)^{n-k}$$
<!--ID: 1715790676120-->


## Théorème de Weierstrass-Bernstein
On énonce le théorème suivant: #!

Pour tout fonction $f: [0, 1] \to \mathbb R$ continue, la suite de [[#Polynômes de Bernstein]] de $f$ converge uniformément vers $f$: $$\lim_{n \to +\infty} \sup_{x \in[0,1]} |f(x) - B_n^f(x)| = 0$$
<!--ID: 1715790676123-->
