## Théorème
On a déjà défini ici le [[Beppo-Levi|théorème de Beppo Levi]], mais nous allons tout de même le réitérer: #!

On se place dans un espace mesuré $(E, \mathcal E, \mu)$, on pose alors $f_{n}: E \to [0, \infty]$ une suite de fonction sur $\mathbb{N}$. On suppose cette suite de fonction croissante, ==DONC==: $f_{n} \leq f_{n+1}$
Ainsi en posant $f = \lim_{ n \to \infty } f_{n}$ on a aussi $f = \sup_{n \in \mathbb{N}} f_{n}$
On a déjà que $f$ est mesurable par limite simple de fonction mesurable, mais aussi que $$
\int_{E}fd\mu = \int_{E}\lim_{ n \to \infty } f_{n}d\mu=\lim_{ n \to \infty } \int_{E} f_{n}d\mu
$$

**Remarque**: Beppo-Levi sert donc à intervertir limite et intégrales


### Preuve
La preuve est longue, et j'ai pas le temps là :D