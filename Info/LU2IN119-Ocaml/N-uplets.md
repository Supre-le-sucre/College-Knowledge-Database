# Accesseurs de couples
Pour les couples, les fonctions `fst` et `snd` renvoie respectivement le premier et le second élément

```ocaml
# (28, "janvier") ;;
- : int * string = (28, "janvier")

# fst (28, "janvier") ;;
- : int = 28

# snd (28, "janvier") ;;
- : string = "janvier"

# fst (28, "janvier", 2021) ;;
Error: This expression has type 'a * 'b * 'c
       but an expression was expected of type 'd * 'e
```