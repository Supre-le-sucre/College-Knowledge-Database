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
