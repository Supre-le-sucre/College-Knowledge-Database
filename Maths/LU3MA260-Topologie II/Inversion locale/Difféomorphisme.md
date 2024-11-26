#topo
## Définition
Soit $\Phi : U \to V$ où $U, V$ respectivement ouvert de $E$ et $F$. On dit que $\Phi$ est un $\mathcal C^1$-difféomorphisme si et seulement si: #!

Elle est de classe $\mathcal C ^1$, bijective et si son inverse est de classe $\mathcal C ^1$

## Théorème
Soit $E$ et $F$ deux espaces de Banach et $f: \Omega \to F$ une fonction de classe $\mathcal C ^1$
Soit $a \in \Omega$ tel que $D_{f}(a) \in \mathcal L(E, F)$ inversible tel que $(D_{f}(a))^{-1} \in \mathcal L(E, F)$: #!

Alors il existe $U,V$, respectivement ouvert de $E$ et $F$ tel que $f: U \to V$ est un $\mathcal C^1$-difféomorphisme.



### Corollaire
Soit $f: \Omega \to F$ de classe $\mathcal C ^1$ sur $\Omega$. Supposons que $\forall a \in \Omega$, et $D_{f}(a)$ suivant les hypothèses du théorème précédent alors: #!

$\forall O$ ouvert de $\Omega$, on a que $f(O)$ est un ouvert de $F$
Si $f$ est injective, alors $f: \Omega \to f(\Omega)$ est un $\mathcal C ^1$-difféomorphisme

#### Preuve
Soit $O$ un ouvert de $\Omega$, a-t-on que $f(O)$ est un ouvert de $F$ ?

Soit $y \in f(O)$, alors $\exists x \in O$ tel que $f(x)=y$. Mais $D_{f}(x)$ est inversible continue et d'inverse continue, donc il existe $U, V$ tel que $U$ est un ouvert contenant $x$ et $V$ un ouvert de $F$ tel que $f:U \to V$ est un difféomorphisme

Donc
$$
\exists \varepsilon > 0, B(x, \varepsilon) \subset U \cap O \text{ et } \left(f^{-1}\right)^{-1}( B(x, \varepsilon)) = f(B(x, \varepsilon)) \subset f(O)
$$
et $f(B(x, \varepsilon))$ est un ouvert tel que $y \in f(B(x, \varepsilon))$. Donc $f(O)$ est ouvert

Pour le deuxième point, supposons cette fois $f$ injective.
Et posons $f: \Omega \to f(\Omega)$ qui est donc bijective avec $f^{-1}: f(\Omega) \to \Omega$ qui vérifie bien que
$$
\forall x  \in f(\Omega), \varepsilon>0 \text{ et } B(x, \varepsilon) \text{ tel que } f^{-1}: B(x, \varepsilon) \to \Omega
$$
est de classe $\mathcal C ^1$, alors $f^{-1}$ est aussi de classe $\mathcal C^1$ sur $f(\Omega)$


