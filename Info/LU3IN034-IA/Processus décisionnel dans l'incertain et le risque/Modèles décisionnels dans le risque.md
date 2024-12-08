(cf. [[Différence entre l'incertain et le risque]])


# Définition d'une loterie
Une loterie est une loi de probabilité $P$ à support finie

# Critère de dominance stochastique d'ordre 1
Dans le risque, les probabilités de chaque état étant connu, on dit qu'un acte $f$ est dominant par rapport à un autre $g$ si sa loterie $X$ est supérieur à l'autre $Y$. Autrement dit
$$
X \text{ domine } Y \quad \Leftrightarrow \quad \forall x \in X \;P(X > x) \geq P(Y > x)
$$

## Exemple
![[Pasted image 20241208231320.png]]
Ici, $X$ ne domine pas $Y$, mais $Y$ ne domine pas non plus $X$

# Aversion au risque
Un agent est qualifié d'adversaire au risque, si pour toute loterie $X$, il préfère un gain certain de $\mathbb E(X)$ que de jouer à $X$

# Equivalent certain
L'équivalent certain d'une loterie $X$ est le gain certain $EC(X)$ tel que $X \sim EC(X)$
Autrement dit, le décideur est indifférent entre, jouer la loterie $X$ ou gagner $EC(X)$

# Modèle de l'utilité espéré dans le risque
Dans le risque, on souhaite comparer deux loterie ensemble $P$ et $Q$, le modèle EU, consiste alors à utiliser un paramètre $\lambda$ et à évaluer l'espérance de gain dans la loterie mixée telle que
$$
\lambda P + (1-\lambda)Q
$$
![[Pasted image 20241208232156.png]]

## Axiome du modèle EU dans le risque
On observe les axiomes suivants

- Comparabilité transitive complète
Toute les loteries $P, Q$ sont comparables
En considérant les loteries $P,Q$ et $R$ on a que $P > Q$ et $Q > R$ implique que $P> R$

- Continuité
Pour toutes loteries $P > Q > R$, il existe $\alpha, \beta \in ]0, 1[$ tel que
$$
\alpha P + (1-\alpha)R > Q \quad \quad Q > \beta P+ (1- \beta)R
$$

- Indépendance
Pour toutes loteries $P, Q, R$, pour tout $\alpha \in ]0, 1]$
$$
P > Q \Leftrightarrow \alpha P + (1-\alpha)R > \alpha Q + (1- \alpha)R
$$

## Théorème de von Neumann et Morgenstern
Si la relation d'ordre sur les loteries respectes les axiomes précédent, alors il existe une fonction d'utilité de loterie $U$ de la forme

$$
U(P) = \sum_{x \in X} P(x) u(x)
$$
où $u$ est une application définie par une transformation affine près et telle que
$$
\forall P > Q \Leftrightarrow U(P) \geq U(Q)
$$

# Utilité de la conséquence
On note $u(x)$ l'utilité de la conséquence $x$ pour l'agent, elle caractérise notamment ses préférence vis à vis du risque.
L'utilité est linéaire pour les probabilité

## Concavité convexité
La concavité de $u$ se traduit comme une aversion du risque, alors que la convexité, comme un goût du risque