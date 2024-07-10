# Définition d'une fonction anonyme
En Ocaml, les fonctions dites "anonymes" (donc sans nom) sont identifiées par le mot clé `function` (On peut aussi utiliser `fun` pour accepter plus d'un seul paramètre paramètres)

```ocaml
# function x -> x+1 ;;
- : int -> int = <fun>

# (function x -> x+1) 2019 ;;
- : int = 2020

# function x -> x < 0 ;;
- : int -> bool = <fun>
```

On peut aussi donner un nom à ses fonctions anonymes avec `let`
```ocaml
# let succ = function x -> x+1 ;;
val succ : int -> int = <fun>

# succ 2 ;;
- : int = 3
```

# Déclaration d'une fonction
On peut déclarer une fonction de 3 façons différentes...
Voici 3 déclarations équivalentes:

```ocaml
# let add1 = function x -> function y -> x + y ;;
val add1 : int -> int -> int = <fun>

# let add2 = fun x y -> x + y ;;
val add2 : int -> int -> int = <fun>

# let add3 x y = x + y ;;
val add3 : int -> int -> int = <fun>
```

# Récursion
Pour définir une fonction récursive en Ocaml, il suffit d'utiliser le mot clé `rec`
```ocaml
# let rec sigma n = if n = 0 then 0 else n + sigma (n-1) ;;
val sigma : int -> int = <fun>

# sigma 10 ;;
- : int = 55
```

## Récursion terminale
Il est souvent recommandé d'utiliser la récursion terminale. Cela signifie que la fonction n'exécute aucune autre instruction après son appel.
Le compilateur optimisera le code, afin de réutilise l'environnement précédent, plutôt que de surcharger la pile.

Voici l'équivalent de la fonction sigma avec une récursion terminale. Remarquons l'utilisations d'une fonction auxiliaire, ainsi que d'un accumulateur, qui garde en mémoire l'environnement précédent.
```ocaml
# let sigma n = 
	let rec sigma_aux n acc = 
		if n = 0 then acc
		else sigma_aux (n-1) (n+acc)
	in sigma_aux n 0 ;;
	
val sigma : int -> int = <fun>

# sigma 10 ;;
- : int 55
```
La définition locale de la fonction auxiliaire permet d'empêcher l'utilisateur de l'utiliser. Ceci protège sa bonne utilisation (Notamment car l'accumulateur doit être géré au départ)

