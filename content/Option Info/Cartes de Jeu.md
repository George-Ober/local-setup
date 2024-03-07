On comprend d'ores et déjà que pour modéliser des cartes, il nous faudra définir des types correspondants.
```ocaml
type valeur =
 | Brele of int
 | Tete of string

type couleur =
 | Pique
 | Coeur
 | Trefle
 | Carreau
```

Et bien évidemment pour définir une carte, il nous faudra donner un couple de deux valeurs

```ocaml
type carte = couleur * valeur
let dame_de_coeur :carte = (Coeur, Tete("Dame"))
let trois_de_pique :carte = (Pique, Brele(3))
```

On commence par écrire une fonction qui vérifie si une carte est rouge
```ocaml
let est_rouge (c :carte) : bool =
	(* Teste si c est rouge *)
	let (clr, _) = c in
	clr = Coeur || clr = Carreau
```

On peut évidemment tester cette fonction avec les deux cartes que l'on a défini.
```ocaml
let test_est_rouge : unit =
    assert(est_rouge dame_de_coeur);
    assert(not(est_rouge trois_de_pique))
```

Mais on peut définir une autre fonction en utilisant le [[pattern matching]]
```ocaml
let est_rouge_filtrage (c :carte) : bool =
	(* Teste si c est rouge *)
	let (clr, _) = c in
	match clr with
	| Carreau -> true
	| Coeur -> true
	| _ -> false
```

Qui est une syntaxe équivalente à 
```ocaml
let est_rouge_filtrage_equivalent (c :carte) : bool =
	(* Teste si c est rouge *)
	let (clr, _) = c in
	match clr with
	| Carreau | Coeur -> true
	| _ -> false
```

Pour se donner une autre idée de comment marche le pattern matching, regardons comment se comporte la syntaxe pour les valeurs définies avec des constructeurs :

```ocaml
let est_un_trois (c :carte) : bool =
	(* Teste si c est un trois *)
	let (_, vlr) = c in
	match vlr with
	| Brele (k) -> k = 3
	| Tete (_) -> false
```

