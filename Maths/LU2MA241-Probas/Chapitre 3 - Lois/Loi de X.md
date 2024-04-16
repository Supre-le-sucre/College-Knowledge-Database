#probas 
## Définition
On définit une loi d'une [[Variables aléatoires discrètes|v.a discrète]] #!
la mesure dite de probabilité $\mu_x: \mathcal{P}(E) \to [0,1]$ 

On appelle la densité discrète de $X$ l'application: #!
$$p_x: E \to [0,1] $$ $$p_x(x) = \mathbb P(X = x) = \mu_x(\{x\})$$
## Propriété
Soit $X: \Omega \to E$ une variable aléatoire discrète. La fonction $p_x$ est une [[Densité discrète]] de $X(\Omega)$ et est nulle en dehors de $X(\Omega)$. 
La loi $\mu_x$ est la probabilité sur $(X(\Omega), \mathcal P(X(\Omega)))$ associée à la [[Densité discrète]] $p_x$ étendue à une probabilité sur $(E, \mathcal P(E))$ par:
$$\mu_x(A) = \sum_{x \in A} p_X(x) = \sum_{x \in A \cap X(\Omega)}p_X(x), \;\; A \in \mathcal P(E)$$

## Indépendances des variables aléatoires
Soit $X_1, \dots, X_n$ définie sur le même espace probabilisé, et à valeurs respectivement dans les ensembles $E_1, \dots, E_n$. On dit qu'elles sont indépendantes si #!
pour tout choix de sous ensemble $A_1 \subseteq E_1, \dots, A_n \subseteq E_n$ on a l'élagalité suivante:
$$\mathbb P(X_1 \in A_1, \dots, X_n \in A_n) = \prod_{i=1}^n\mathbb P(X_i \in A_i)$$

### Remarque importantes sur l'indépendance
On note ces points importants sur l'indépendance d'une variable aléatoire discrète: #!
L'indépendance d'une variable aléatoire est conservé par application d'une fonction sur celle-ci. De fait la somme de variables aléatoires indépendantes est aussi indépendante avec la somme d'autres variables aléatoires indépendantes.