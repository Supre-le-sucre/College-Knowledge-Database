#algo

Un [[Graphes]] est dit orienté, si toutes ses arrêtes connectent les sommets dans les 2 sens.

## Chaînes particulières

On définit un ==cycle==, une chaîne fermée (i.e tel que $v_{n+1} = v_1$)
Un cycle est dit ==élémentaire== s'il s'agit d'une [[Graphes#Chaîne|chaîne élémentaire]] fermée

Un graphe non orienté est dit ==connexe== s'il existe pour tout couple de sommet $(v, u) \in V^2$, une chaîne élémentaire entre $u$ et $v$ (i.e, [[Graphes#Chaîne|rappellons le]], il existe une connexion entre un sommet et un autre, même indirect)

### Composantes connexes
On appelle composantes connexes, l'ensemble des sommets de $G$ induisant $SG$, un sous graphe connexe.
