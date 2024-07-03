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

En Ocaml on peut aussi faire `[1; 2] @ [3; 4]` donne `[1; 2; 3; 4]`