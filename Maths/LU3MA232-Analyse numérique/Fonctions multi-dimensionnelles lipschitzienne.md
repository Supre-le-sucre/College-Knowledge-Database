## Définition
On dira que pour $f(t, y)$, la fonction est Lipschitzienne de constante $L$ si #!
$$\forall t \in I, \forall y_1, y_2 \in \Omega$$ $$||f(t, y_1) - f(t, y_2)|| \leq L||y_1 -y_2||$$

## Définition
On dira que pour $f(t, y)$, la fonction est localement Lipschitzienne de constante $L$ si #!

$$\forall t_0 \in I, \forall y_0 \in \Omega, \forall r \text{ tel que } [t_0 -r, t_0+r] \subset I, B_f(y_0, r) \subset \Omega$$
$$\forall t \in [t_0-r, t_0+r], \forall y_1, y_2 \in B_f(y_0, r)$$$$||f(t, y_1) - f(t, y_2)|| \leq L||y_1 -y_2||$$Cette situation arrive lorsqu'on ne peut majorer $||f(t, y_1) - f(t, y_2)||$ que par un $L$ dépendant de $t$ sur tout $I$ et $\Omega$ 

## Propriété
Si $f$ est de classe $\mathcal C^1$, on peut en déduire des choses sur sa caractérisation lipchitzienne: #!

- Si $f'$ est bornée, alors $f$ est lipchitzienne de constante $\sup f'$.
- Si on n'a rien à d'autre à dire, on peut au moins dire qu'elle est Lipchitzienne.
Ceci vient de [[Taylor-Lagrange#Théorème des accroissements finis|Théorème des accroissement fini]]. Cette propriété se gén,éralise dans les dimensions supérieures.