### Corollaire
On peut déduire qu'un espace est connexe de la façon suivante: #!
Un espace connexe par arcs est connexe ==La réciproque est fausse==

#### Preuve
Supposons que $X$ est non connexe, donc $X=O \sqcup O'$, avec $O \cap O' = \emptyset$ 
Trivial.


## Opérations sur les connexes
On observe la stabilité suivante: #!

1) L'image d'un connexe par une fonction continue est connexe
2) L'union de deux connexes d'intersections non vide est connexe
3) Le produit de deux connexes est connexe

### Preuve

Pour 1) On montre la contraposée
Soit $f: X \to Y$ avec $f(X) = Y$ une fonction continue et supposons $Y$ non connexe
Alors $Y = O \sqcup O'$, montrons que $X$ est non connexe

Or il suffit de poser $\tilde{O} = f^{-1}(O)$ et $\tilde{ O'} = f^{-1}(O')$. Comme il s'agit d'une application continue, la pré image d'un ouvert est un ouvert. Et ces ouverts sont disjoints et forment $X = \tilde{O} \sqcup \tilde{ O'}$.

Pour 2) On pose $X_{1}, X_{2}$ deux espaces connexes tel que $X_{1} \cap X_{2} \neq \emptyset$. ON va montre que $X_{1} \cup X_{2}$ est connexe.
Montrons donc que pour tout application continue $f$, la fonction $f: X_{1} \cup X_{2} \to \{0,1\}$ est constante.
On a alors que les restrictions $f_{|X_{1}}$ et $f_{|X_{2}}$ sont continues.
Comme $X_{1}$ et $X_{2}$ connexes, on a alors que $f_{{|X_{1}}} = c_{1}$ et $f_{{|X_{2}}} = c_{2}$. Or comme l'intersection entre $X_{1}$ et $X_{2}$ est non vide, il partage un point donc $c_{1} = c_{2}$, d'où $f$ constante sur $X_{1} \cup X_{2}$ et donc $X_{1} \cup X_{2}$ connexe

Pour 3) la preuve est un peu plus délicate
Posons $X_{1}$ et $X_{2}$ connexes et montrons que $X_{1} \times X_{2}$ est connexe

Soit $X_{1} \times X_{2} = O \cup O'$ avec $O$ et $O'$ ouvert et $O \cap O' = \emptyset$, on montre alors que $O = X_{1} \times X_{2}$ ou $O' = X_{1} \times X_{2}$

Soit $x_{2} \in X_2$ et soit $Y_{x_{2}} = X_{1} \times \{x_{2}\}$
$\forall x_{2} \in X_{2}$ on a que $Y_{x_{2}}$ est un espace connexe, car en effet, $f: Y_{{x_{2}}} \to \{0, 1\}$
est constante car $X_{1}$ est connexe et il suffit de prendre $\tilde{f}: X_{1} \to \{0, 1\}$ avec $\tilde{ f}(x) =f(x, x_{2})$ pour s'en convaincre.

On a donc nécessairement $X_{1} \times \{x_{2}\} \subset O \sqcup O'$ .
En effet, $\tilde{ O} = X_{1} \times \{ x_{2} \}$