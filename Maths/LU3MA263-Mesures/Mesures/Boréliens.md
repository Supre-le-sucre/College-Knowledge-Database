## L'intersection de tribu
Soit $\mathcal E_i$ avec $i \in I$ des tribus sur $E$. Alors:
$$\mathcal E = \bigcap_{i \in I}\mathcal E_i$$est encore une tribu de $E$.
**Remarque**: En général, l'union de tribu ne forme pas de tribu

### Preuve
On vérifie que $\mathcal E$ est une tribu...

i) $\forall i \in I$, $E \in \mathcal E_i$ car les $\mathcal E_i$ sont des tribus
Donc $E \in \bigcap \mathcal E_i$

ii) Soit $A \in \mathcal E$, montrons que $A^c \in \mathcal E$
Si $A \in \mathcal E$, alors $A \in \mathcal E_i$ pour tout i. Mais $\mathcal E_i$ sont des tribus, donc, $A^c \in \mathcal E_i$ pour tout i

iii) Soit $A_n \in \mathcal E$, on a donc que pour tout i et n $A_n \in \mathcal E_i$
Or comme les $\mathcal E_i$ sont des tribus, $\bigcup A_n \in E_i$ pour tout i