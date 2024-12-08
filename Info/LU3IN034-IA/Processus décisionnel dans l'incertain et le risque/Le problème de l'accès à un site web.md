On pose le problème suivant

Un agent recherche un ensemble de document sur le web. Il tombe sur le site $S$ dont les données sont mal connus. Cependant, ces données pourrait avoir de l'importance

La qualité du site est probabilisé comme
- Mauvaise dans 27% des cas
- Moyenne dans 30% des cas
- Bonne dans 43% des cas

Si la qualité du site est mauvaise, les documents récupéré n'ont aucune valeur.
Si elle est moyenne, elles ont une valeur de 750, et si elle est bonne de 900.

Le site est payant et demande un coût d'accès de 500

L'arbre de décision est le suivant
![[Pasted image 20241209003022.png]]
$S$ représente l'action de payer pour l'accès au site, et $S'$ l'action de ne rien faire.
L'espérance de gain est de 112 en ayant la politique de payer pour l'accès au site.

On aimerait tenter de mieux s'informer, mais toute information a un prix... Tentons d'évaluer la valeur de l'information parfaite.
Pour cela, on étudie l'arbre de décision inverse: cet arbre représente le cas où l'information est parfaite: imaginons donc, que l'on sait à l'avance la qualité du site
![[Pasted image 20241209003300.png]]
L'espérance de gain est alors à 247, la valeur de l'information parfaite est donc de 247-112 = 135

Un informateur, qui a déjà travaillé avec le site web que l'on étudie, nous propose ses services
L'informateur a une probabilité de nous indiquer s'il faut acheter ou ne pas acheter les informations. Ses conseils sont associés aux probabilités conditionnels suivantes

|                                          | $I_{1}$: "Acheter l'accès au site" | $I_{2}$: "N'achetez pas les accès" |
| ---------------------------------------- | ---------------------------------- | ---------------------------------- |
| $s_{1}$: Le site est de mauvaise qualité | 44%                                | 56%                                |
| $s_{2}$: Le site est de moyenne qualité  | 60%                                | 40%                                |
| $s_{3}$: Le site est de bonne qualité    | 81%                                | 19%                                |
*Par exemple la première case se lit: la probabilité que l'informateur nous disent d'acheter le site, sachant que celui-ci est de mauvaise qualité est de 44%*

Le coût de service de l'informateur est de $c$
En utilisant les lois de probabilités Bayésienne
$$
P(s_{j} | I_{k}) = \frac{P(I_{k}| s_{j}) P(s_{j})}{P(I_{k})} = \frac{P(I_{k}| s_{j}) P(s_{j})}{\sum_{i}P(I_{k}|s_{i})P(s_{i})}
$$

Il est possible de dresser l'arbre de décision suivant, où le nœud de départ représente la décision de payer l'informateur ou non.
![[Pasted image 20241209004446.png]]
L'arbre en haut est le même que le précédent, c'est le cas où nous n'avons pas choisi de payer l'informateur

L'arbre en bas représente la version où nous avons payé l'informateur.
Ici l'informateur est viable s'il ne coûte que 127-112 = 15, autrement, ses informations coûterait trop cher.