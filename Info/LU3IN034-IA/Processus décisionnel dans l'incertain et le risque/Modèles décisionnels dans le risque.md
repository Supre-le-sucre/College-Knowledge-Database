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