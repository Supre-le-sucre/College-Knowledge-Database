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