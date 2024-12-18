## Formalisme décisionnel dans l'incertain total
On note

- $S$ l'ensemble des états de la nature
- $2^{S}$ l'ensemble des événements
- $X$ l'ensemble des conséquences
- Un acte, comme une fonction $f: S \to X$

## Formalisme décisionnel dans le risque
Dans le risque, contrairement à l'incertain, on connaît la loi de probabilité
$P: 2^{S} \to [0, 1]$.
Ainsi, pour tout acte $f$ on peut établir la loi de probabilité $P_{f}: 2^{S} \to [0, 1]$ et tel que
$$
P_{f}(x) = P(\{ s \in S: f(s) = x \})
$$

## Exemple
On considère deux jeux de dès, le jeu $f$ et le jeu $g$, chacun on des gains différents suivant la valeur du dé

**Pour le jeu** $f$

| valeur du dé | gain |
|--------------|------|
| 1            | 1    |
| 2            | 0    |
| 3            | 1    |
| 4            | 0    |
| 5            | 1    |
| 6            | 0    |
**Pour le jeu** $g$

| valeur du dé | gain |
| ------------ | ---- |
| 1            | 1    |
| 2            | -1   |
| 3            | 0    |
| 4            | 3    |
| 5            | -1   |
| 6            | 0    |
En réalité, les jeux $f$ et $g$ sont des actes. Pour chaque état (la valeur du dé), il y a une conséquence (le gain associé)

**Dans l'incertain total**, on ne sait rien sur le dé, il pourrait être pipé... 
On va donc comparer les actes entre eux, et vérifier lequel est le plus profitable

![[Pasted image 20241208221508.png]]

**Dans le risque**, on peut imaginer le cas où le dé est équilibré. Auquel cas, on ne compare plus les actes, mais **la probabilité des gains selon les actes** (loi de probabilité sur $X$)

![[Pasted image 20241208222245.png]]