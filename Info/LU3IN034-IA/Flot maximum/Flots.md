## Définition du flot
Un flot est une application sur les sommets d'un [[Graphes de capacité]] $f: V^2 \to \mathbb R$ avec les conditions: #!
- Antisymétrique: $f(u,v) = -f(v,u)$
- Conservation $\forall u \not = \set{s, t} \in V, \sum_{v \in V} f(u,v) = 0$
- Capacité: $\forall u, v \in V f(u,v) \leq c(\{u,v\})$
Un arc est dit saturé si $f(u, v) = c(u, v)$
**ATTENTION** : ==Tout ce qui rentre dans un sommet (à part la source et le puits), ressort==
<!--ID: 1726076885860-->


### Valeur du flot
Dans un graphe, la valeur du flot $f$, notée $|f|$ est donnée par: #!
$$|f| = \sum_{v \in V} f(s, v) = \sum_{u \in V} f(u, t)$$
<!--ID: 1726076885870-->


# Flot maximum - [[Coupe]] minimum

## Définition
Un flot est dit maximum, s'il existe une coupe $(A,B)$ tel que la capacité de cette coupe est égale au flot

## Lemmes
Pour donner le théorème du flot maximum-coupe minimale, il nous faut définir les 4 lemmes suivants concernant le flot et le [[Graphes d'écart (ou résiduel)]]: #!

a) $f'$ est un flot dans $G_f$ ([[Graphes d'écart (ou résiduel)|graphe d'écart]]) si et seulement si $f+f'$ est un flot dans $G$
b) $f'$ est un flot maximal dans $G_f$ si et seulement si $f +f'$ est un flot maximal dans $G$
c) $|f \pm f'| = |f| \pm |f'|$
d) Si $f$ un flot quelconque et $f^*$ un flot maximum de $G$ alors la valeur du flot maximal dans $G_f$ est égale à $|f^*| - |f|$
<!--ID: 1726076885879-->



## Théorème flot maximum-coupe minimale
Les assertions suivantes sont équivalentes: #!

i) $f$ est un flot maximum de $G= (V, E, c)$
ii) Il existe une coupe maximum $(A, B)$ telle que $c(A, B) = |f|$
iii) Il n'existe pas de chemin augmentant dans $G_f$
<!--ID: 1726076885888-->


## Algorithme de Ford & Fulkerson

a) On commence par un flot de valeur 0
b) On détermine un chemin augmentant $p$ dans $G_f$ et on pousse $d$ unités supplémentaires de $s$ à $t$ (avec $d$ la capacité [[Graphes d'écart (ou résiduel)|résiduelle]] minimale entre les arcs)
c) On continue jusqu'à ce qu'il n'existe plus de chemin augmentant sur $G_f$

Pour éviter de tracer le graphe d'écart, on peut procéder comme suit:
```
marquer s d'un +
	répéter jusqu'à ce que t soit marqué
		Si il existe e = (u,v) avec u marqué et v non marqué et f(e) < c(e)
			alors marquer v d'un + et père(v) <- u
		Sinon
			Si il existe e = (u,v) avec v marqué et u non marqué et f(e) > 0
			alors marquer u d'un - et père(u) <- v
```

### Complexité
La complexité de l'algorithme de Ford et Fulkerson est tel que: #!
Le flot maximum est obtenu au bout d'au plus $O(|f^*|)$ étapes d'augmentation
<!--ID: 1726076885898-->

# Pré-flots

## Définition
Soit $G = (V, E, c)$. On définit un pré-flot: #!

Une fonction $f: E \to \mathbb R^+$ telle que: $$\forall e \in E, 0 \leq f(e) \leq c(e)$$$$\sum_{e \text{ entrant à } v}f(e) \geq \sum_{e \text{ sortant à } u} c(e)$$
