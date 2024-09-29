## Définition
Pour un espace métrique $X$, on dit que $F$ est fermé lorsque: #!

Son complémentaire $F^c$ est [[Notions d'ouvert par les distances|ouvert]] 

## Propriété de stabilité d'un fermé
On observe la propriété suivante: #!

- Une intersection finie ou infinie de fermés est un fermé
- Une ==union finie== de fermés est un fermé
**Remarque**: C'est le complémentaire de la [[Notions d'ouvert par les distances#Intersection et union d'ouverts|propriété sur les ouverts]]

## Définition de l'adhérence
Soit $(X,d)$ un espace métrique muni d'un ensemble $E \subseteq X$. #!

On appelle adhérence de $E$, noté $\overline{E}$, l'ensemble donné par l'intersection de tous les fermés de $F \supseteq E$.
**Remarque**: On a toujours que $E \subseteq \overline{E}$ et que $\overline{E}$ est un fermé.

## Propriété de l'adhérence
On a que $x \in \overline{E}$ si et seulement si: #!
$$B(x, \epsilon) \cap E \not = \emptyset$$

## Propriété sur la continuité et les fermés
Soient $X$ et $Y$, 2 espaces métriques et $F: X \to Y$ alors: #!

$f$ est continue sur $X$ si et seulement si, $\forall F$ fermé de $Y$, $f^{-1}(F)$ est un fermé de $Y$


## Définition d'un espace dense
Dans un espace métrique $(X, d)$, on dit que $A \subseteq X$ est dense dans $X$ lorsque: #!
$$\overline{A} = X$$
