# Longueur de listes
On peut poser la fonction mathématique suivante: $$\begin{cases} \text{(length [])} & = 0 \\ (\text{length}\; x::xs) & = 1 + (\text{length}\; xs) \end{cases}$$
On peut donner les fonctions en Ocaml suivantes:
```ocaml
let rec length(l: 'a list) : int =
	if l = [] then 0
	else 1 + (length List.tl l) ;;
```
Ici on utilise la fonction `tl` qui permet de continuer dans la liste (c'est la queue de la cellule courante qui est `l`)

Ou alors:
```ocaml
let rec length(l: 'a list) : int = 
	match l with
		| [] -> 0
		| x::xs -> 1 + length(xs) ;;
```
Ou cette fois on utilise la syntaxe `::`

## Récursion terminale de la longueur
```ocaml
let rec length_aux len l =
	match l with
		| [] -> len
		| a::l -> length_aux (length + 1) l ;; 

let length l = length_aux 0 l ;;
```

# Appartenance à une liste

```ocaml
let rec mem (z: 'a) (xs: 'a list) : bool =
	match xs with
		| [] -> false
		| x::xs -> (x = z) || (mem z xs) (* xs en paramètre a été écrasé *) ;;
```

# Ajouter des éléments à une liste
$$\begin{cases}
(append \;[] \;ys) & = ys \\
(append \;(x::zs)\; ys) & = x :: (append \;zs::ys) 
\end{cases}
$$

```ocaml
let rec append(xs: 'a list) (ys: 'a list): ('a list) = 
	match xs with
		| [] -> ys
		| x::xs -> x :: (append xs ys) ;;
```
En Ocaml on peut aussi faire `[1; 2] @ [3; 4]` pour avoir la liste `[1; 2; 3; 4]`


## Récursion terminale `append`
```ocaml
let rec rev_append l1 l2 =
	match l1 with
		| [] -> l2
		| a::l -> rev_append l (a::l2) ;; (* Il faut inverser la liste ! *)

let rev l = rev_append l [] ;;
```

# Le `map`

```ocaml
let rec map f l = 
	if l = [] then []
	else (f (List.hd l)) :: (map f (List.tl l)) ;;
```

```ocaml
let rec map f l = 
	match l with
		| [] -> []
		| t::q -> (f t) :: (map f q) ;;
```

## Exemple intéressant
```
# map (append [10; 20]) [[3; 4; 5]; [8; 3; 1]]
- : int list list = [[10; 20; 3; 4; 5]; [10; 20; 8; 3; 1]]

# map ((@) [10; 20]) [[3; 4; 5]; [8; 3; 1]]
- : int list list = [[10; 20; 3; 4; 5]; [10; 20; 8; 3; 1]]
```

Utiliser `(@)` permet de l'utiliser en mode préfixe `(@) [1; 2] [3; 4]` est équivalent `[1; 2] @ [3; 4]`

# Le n-ième élément d'une liste

```ocaml
let rec nth (l: 'a list) (i: int) : 'a = 
	match l with
		| [] -> raise (Failure "nth")
		| x::xs -> if i=0 then x else (nth xs i-1) ;;
```