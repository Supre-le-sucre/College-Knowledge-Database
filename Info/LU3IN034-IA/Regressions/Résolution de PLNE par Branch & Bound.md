Pour résoudre un PLNE, on peut scinder le problème en 2. Le principe est alors le suivant.

- Relaxer le problème en un PL classique sur $\mathbb{R}^+$ et calculer une solution optimale à ce problème que l'on note $\hat{x}$ 
- Pour toutes les variables non entières qui compose $\hat{ x}$ en choisir une et tester deux nouveaux PL relaxe dans la quelle on ajoute la contrainte
$$
\hat{x_{k}} \leq \lfloor \hat{x_{k}} \rfloor \quad \text{ ou } \quad \hat{ x_{k}} \geq \lceil \hat{x_{k}} \rceil    
$$
- On résous les deux nouveaux PL, et si l'un est plus prometteur que l'autre on poursuit dans sa branche

## Exemple
On pose le PLNE suivant
![[Pasted image 20241130141139.png]]
On le relaxe en autorisant $x_{1}, x_{2} \in \mathbb R^+$
On obtient la solution initial $x_{1} \approx 4.65$ et $x_{2} \approx 2.90$ avec $z \approx 19.75$.
On a alors que la solution du PLNE est au moins majorée par $19$

On scinde en 2, actuellement comme les deux variables ne sont pas entières on a le choix
Si on ajoute la contrainte $x_{2}\leq 2$ au PLNE relaxé, alors on obtient un PL qui majore le PLNE à 17
Mais si on ajoute $x_{2} \geq 3$, la majoration reste à 19. C'est cette branche qu'on souhaite explorer.
Cette fois $x_{2}$ est entier dans la résolution du PL, donc la seul variable à contraindre est $x_{1}$ etc.
![[Pasted image 20241130141128.png]]

