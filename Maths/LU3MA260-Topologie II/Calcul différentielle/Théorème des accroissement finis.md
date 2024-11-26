#topo
## Théorème des accroissements finis
On pose le théorème suivant: #!

Soit $f: [a,b] \to F$ dérivable sur $]a,b[$ en supposant qu'il existe $M$ tel que $$
|| f'(x)||_{\infty} \leq M
$$
Alors on a l'inégalité suivante:
$$
||f(b) - f(a)||_{\infty} \leq M(b-a)
$$
<!--ID: 1732560518165-->


### Preuve
Consulter Poly.

## Corollaire
Par rapport au théorème des accroissements finis, soit $f: \Omega \to F$ avec $\Omega$ ouvert, tel qu'il existe $(a,b) \in \Omega$ avec $[a,b] \subset \Omega$: #!

1)
$$\exists M, \forall x \in [a,b], ||D_{f}(x)|| \leq M \implies ||f(b) -f(a)|| \leq M||b-a||$$
2)
$$
\exists M, \forall x \in [a,b], ||D_{f}(x) -D_f(a)|| \leq ||f(b)-f(a)-D_{f}(a)(b-a)|| \leq M \implies M||b-a||
$$
<!--ID: 1732560518168-->

## Preuve
(1) Voir Poly

(2) On applique (1) avec $g(x) = f(x) - D_{f}(a)(x-a)$ en effet $D_{g}(x) = D_{f}(x) - D_{f}(a)$

## Corollaire
Soit $\Omega$ un ouvert connexe, et $f: \Omega \to F$ si $D_{f}(x)=0, \forall x \in \Omega$: #!
Alors $f$ est constante.

### Preuve
Soit $a \in f(\Omega)$ et montrons que $\forall x \in \Omega, f(x)= a$

Si on arrive à montrer que $f^{-1}(\{ a \})$ est à la fois ouvert et fermé, comme $\Omega$ est connexe, alors dans ce cas $f^{-1}(\{ a \}) = \emptyset$ ou bien $f^{-1}(\{ a \}) = \Omega$

Comme $f$ est continue (car différentiable en tout point), alors $f^{-1}(\{ a \})$ est un fermé. Il ne reste plus qu'à montrer qu'il est ouvert.

Soit $x \in f^{-1}(\{ a \})$. Come $\Omega$ est ouvert, $\exists \varepsilon>0$ tel que $B(x, \varepsilon) \subset \Omega$.
Or comme $D_{f}(x) = 0$ pour tout $x \in \Omega$, on peut majorer par le TAF la norme suivante
$$
\forall z \in B(x, \varepsilon), \quad ||f(z)-f(x)|| \leq 0 \times||z-x|| \leq 0
$$
Donc $f(z)= a, \forall z \in B(x, \varepsilon)$, donc $B(x, \varepsilon) \subset f^{-1}(\{  a \})$ donc c'est bien un ouvert.