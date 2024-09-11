Etant donné un ensemble de préférence de couple (simplifié par hommes et femmes). On cherche à concevoir un processus de couplage dit **stable**

## Paire instable
Une paire $(x, y)$ (homme et femme) est qualifié de *instable* si: #!

- l'homme $x$ préfère la femme $y$ que sa femme actuelle
- la femme $y$ préfère l'homme $x$ que son homme actuel
Autrement dit, une paire est instable si elle améliore les conditions de $x$ ou $y$. 
On dit qu'une affectation est stable, s'il n'existe pas de paire instable.

## Algorithme de Gale-Shapley
L'algorithme suivant permet de garantir un couplage stable: #!

```
Initialiser chaque personne comme libre.
tant que (il existe un homme libre qui n'a pas proposé à toutes les femmes): 
	Choisir un tel homme
	w = 1ere femme de la liste n'ayant pas été proposée

	si (w est libre)
		considérer m et w comme fiancé
	sinon si (w préfère m à son fiancé m')
		considérer m et w comme fiancé, et m' comme libre
	sinon
		w rejette m
```

### Preuve de terminaison

On observe d'après l'algorithme que:
- Les hommes proposent aux femmes dans l'ordre décroissant de leurs préférences
- Quand une femme est couplée, elle le reste pour toujours
- Au cours de l'algorithme, le partenaire de la femme "s'améliore"

Dans la boucle, à chaque itération, un homme propose à une nouvelle femme, il existe au plus n² combinaisons possibles.
$$\tag*{$\blacksquare$}$$

### Preuve de couplage parfait
On suppose, par contradiction, qu'il existe un homme $m$ qui n'a pas de couple à la fin de l'algorithme

Comme il y a autant d'homme que de femme, il existe une femme $w$ qui n'est pas en couple
Or l'homme $m$ est censé avoir proposé à toutes les femmes, dont $w$. Donc $m$ et $w$ ont dû être ensemble au moins une fois
Ceci contredit l'hypothèse de départ
$$\tag*{$\blacksquare$}$$

### Preuve de la stabilité
Supposons, encore une fois par contradiction, qu'il existe une paire instable notée $(m, w)$ dans $S^*$ l'ensemble des couples stables obtenu par l'algorithme.

On distingue 2 cas:
- $m$ n'a jamais proposé à $w$
	$m$ propose donc à $w$ et $(m,w)$ devient stable **contradiction**
- $m$ a déjà proposé à $w$
	$w$ rejette $m$ et préfère $m'$
	$(m,w)$ devient alors stable **contradiction**
$$\tag*{$\blacksquare$}$$
### Preuve de l'homme-optimale
On dit que l'algorithme est homme-optimale car: #!
Il accorde aux hommes la meilleure partenaire possible qui est stable

Supposons par l’absurde que ce ne soit pas le cas:
On pose alors $(m, w) \in S^*$ où $w$ n'est pas le meilleur partenaire pour $m$
Comme $m$ propose dans l'ordre décroissant des préférences, $m$ a été rejeté par sa meilleure partenaire $w'$
On a donc $(m', w') \in S^*$ avec $w'$ qui préfère $m'$ à $m$

On pose $(m, w') \in S$ où $S$ est un ensemble de couple stable. C'est possible car $w'$ est la meilleure femme pour $m$
Dans $S$, on pose alors $(m', w)$ car il faut que tout le monde ait un couple

Or $w'$ préfère $m'$ à $m$


