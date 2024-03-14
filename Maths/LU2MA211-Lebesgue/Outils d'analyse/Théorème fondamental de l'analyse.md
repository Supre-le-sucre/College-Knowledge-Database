#lebesgue 

# ==Théorème==
On énonce le théorème fondamental de l'analyse comme suit #!

Soit $f : [a,b] \to \mathbb C$ une fonction continue.
Alors la fonction $F : [a,b] \to \mathbb C$ définie comme suit:
$$F: x \mapsto\int_a^x f(t)dt$$
a pour dérivée $f$
On dit que $F$ est ==la== primitive de $f$ s'annulant en a
<!--ID: 1710446551969-->


## Corollaire
Le théorème fondamental de l'analyse a l'implication fondamentale suivante permettant au calcul d'une intégrale: #!

Si $F: [a,b] \to \mathbb C$ une fonction de classe $\mathcal C^1$ avec $F' = f$, alors
$$\int_a^b f(x)dx = F(b) -F(a)$$
<!--ID: 1710446551973-->


## Corollaire Intégration par partie
On définit l'intégration par partie comme suit: #!

Soit $a < b \in \mathbb  R$ et $f,g :[a,b]\to \mathbb C$ de classe $\mathcal C^1$ et de dérivée respective
Alors: $$\int_a^bf(x)g'(x)dx = [f(x)g(x)]^b_a - \int_a^bf'(x)g(x)dx$$
<!--ID: 1710446580415-->
