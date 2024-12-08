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
L'informateur a une probabilité de nous indiquer s'il faut acheter ou ne pas acheter les informations.
Il a les probabilités suivantes