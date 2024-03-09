Fichiers d'extension `.ml`.
OCaml est un langage de programmation à la fois adapté pour la programmation [[Programmation Fonctionnelle|fonctionnelle]], [[impérative]], [[orientée objet]].

Ce langage possède son propre gestionnaire de paquets, [opam](https://opam.ocaml.org/) depuis lequel il est possible d'installer outils et librairies.

Ce langage peut être **compilé** et **interprété**, on le compile avec `ocamlc`
```sh
ocamlc <file> -o <output>
```

Et on peut l'interpréter dans l'environnement `utop`, en utilisant la directive `#use`.

OCaml est un langage **[[statiquement typé]]**, et muni d'un moteur d'inférence de type capable de déterminer le type d'une fonction, valeur, expression si elle n'est pas précisée[^1].

[^1]: Le moteur d'inférence de type sera *de toute façon* utilisé pour vérifier la cohérence du type annoncé avec le type de l'expression

>[!warning] On vérifiera cependant à préciser le typage de toutes nos fonctions.

Enfin, un fichier `.ml` est constitué d'une succession de définitions.

## Syntaxe des définitions en OCaml

### Définition de valeurs

En général, on définit une valeur par son identifiant
```ocaml
let id_var :type = expression
```
Avec `expression` de type `type`.

### Définition de fonctions

```ocaml
let id_f (arg1 :t1) (arg2 :t2) (argn :tn) :t =
	exp1
```
où :
- `id_f` est l'identifiant
- `arg1` ... `argn` sont les arguments
- `t1` ... `tn` les types des arguments
- `exp1` une expression de type `t` pouvant faire apparaitre `arg1` ... `argn`

#### Fonction récursive
```ocaml
let rec nom_f (arg1 :t1) (arg2 :t2) (argn :tn) :t =
	e
```

où :
- `nom_f` est l'identifiant
- `arg1` ... `argn` sont les arguments
- `t1` ... `tn` les types des arguments
- `e` une expression de type `t` pouvant faire apparaitre `arg1` ... `argn` **ainsi que** `nom_f`

#### Fonctions mutuellement récursives

```ocaml
let rec f1 (arg1 :t1) (arg2 :t2) (argn :tn) :t =
	e1
and f2 (barg1 :ta) (barg2 :tb) (bargm :tm) :t_prime =
	e2
```

où :
- `f1` et `f2` sont les identifiants respectifs des deux fonctions
- `arg1` ... `argn` sont les arguments de `f1`
- `barg1` ... `bargm` sont les arguments de `f2`
- `t1` ... `tn` les types des arguments de `f1`
- `ta` ... `tm` les types des arguments de `f2`
- `e1` une expression de type `t` pouvant faire apparaitre `arg1` ... `argn` **ainsi que** `f1` et `f2`
- `e2` une expression de type `t_prime` pouvant faire apparaitre `barg1` ... `bargm` **ainsi que** `f1` et `f2`

## Expressions en OCaml
>[!quote] Définition
>À un instant donné on appelle "environnement courant" l'ensemble des valeurs, fonctions et types définis.

Pour un environnement donné, une expression est un texte formaté selon la syntaxe OCaml auquel on peut donner un type et une valeur.

>[!warning] Deux expressions ne sont pas identiques parce qu'elles sont du même type et ont la même valeur

### Les constantes

| Type     | Exemple             | Remarque                       |
| -------- | ------------------- | ------------------------------ |
| `unit`   | `()`                | `()` est l'unique valeur       |
| `bool`   | `true`, `false`     | Uniques valeurs                |
| `int`    | `1`, `2`, `-4`, `0` |                                |
| `float`  | `3.` `4.` `0.`      | La notation `.5` n'existe pas. |
| `char`   | `'m'` `'\n'`        |                                |
| `string` | `"mp1"`             |                                |

### Les valeurs
Communément appelées à tort "variables" les valeurs définies dans un environnement courant sont des expressions : après avoir executé
```ocaml
let a = 2
```
`a` est une expression

#### Les arguments
Sont évalués dans les corps de fonction comme des valeurs

### Les opérations

| type 1   | type 2   |                            | type sortie |
| -------- | -------- | -------------------------- | ----------- |
| ` int`   | `int`    | `*` `+` `/` [^2] `mod` `-` | `int`       |
| `'a`     | `'a`     | `<>` `:` `<` `<=` `>` `>=` | bool        |
| `float`  | `float`  | `*.` `+.` `/.` `**` `-.`   | `float`     |
| `bool`   | `bool`   | \|\| `&&`                  | `bool`      |
| `bool`   | ---      | `not`                      | `bool`      |
| `string` | `string` | `^`                        | `string`    |

[^2]: C'est la division euclidienne
### Les appels de fonction
```ocaml
nomf arg1 arg2 argn
```
Où:
- `nomf` est le nom d'une fonction à n arguments de types `t1`, `t2`... `tn` et de type de sortie `t`
- Pour `i`$\in [ \! [ 1, n ] \!]$  `argi` est une expression de type `ti`
Forme une expression de type `t`.

### Les alternatives
```ocaml
if cond then e1 else e2
```
Où:
- `cond` est une expression de type `bool`
- `e1` et `e2` sont deux expressions de même type t
Forme une expression de type `t` et de valeur la valeur de `e1` si la valeur de `cond` est `true`, et la valeur de `e2` sinon.

### Les n-uplets
```ocaml
e1, e2, en
```
Où, pour `i`$\in [ \! [ 1, n ] \!]$, `ei` est une expression de type `ti`.
Cela forme une expression de type `t1 * t2 * ... * tn`

### Les définitions locales
```ocaml
let id = e in e1
```
Où:
- `e` est une expression de type `t`
- `e1` est une expression de type `t1` qui peut utiliser `id`
Forme une expression de type `t1` et de valeur la valeur obtenue en évaluant `e1` où `id` a pour valeur celle de l'expression `e`.


## Définir des types
### Syntaxe de la définition
```ocaml
type id = expression_de_type
```
Où:
- `id` est un identifiant qui commence par une minuscule
- `expression_de_type`
### Expressions de type déjà vues
#### Expressions simples
- On retrouve ici les types de base : `unit` `bool` `float` `int` `char` `string`
- Mais aussi les noms des types que l'on a défini au préalable:
```ocaml
type truc = int
```

#### Expressions de type composées
Pour les *n-uplets*
```ocaml
t1 * t2 * tn
```

Pour une fonction à n arguments de type respectifs `t1`, `t2` et de type de sortie `tn`
```ocaml
t1 -> t2 -> tn
```

Par exemple

```ocaml
type 'a triplet = 'a * 'a * 'a
```

Permet de factoriser tous les types de triplets
```ocaml
let triplet_entiers = int triplet;;
```

### Types paramétrés
>[!quote] Définition
>On peut définir un type dont l'expression dépend d'une variable de type grâce à la syntaxe suivante :

```ocaml
type 'var id = e
```
Où:
- `var` est un identifiant local
- `id` est un identifiant
- `e` est une expression qui peut faire apparaitre le type `'var`

On pourra aussi définir un type dont l'expression dépend de plusieurs paramètres :

```ocaml
type ('v1, 'v2, 'vn) id = e
```

Dans les deux cas, on parle de types paramétrés, et après de telles définitions, on obtient de nouvelles expressions de type en remplaçant les `'v` par :
- `'un_autre_id`
- une expressions de type

```ocaml
type ('a, 'b) triplet_special = 'a * 'b * 'a
type triplets_entiers = (int, int) triplet_special
```

### Types somme et filtrage
![[Cartes de Jeu]]

La syntaxe d’un filtrage par motif est la suivante :
```ocaml
match expr0 with  
| motif1 −> expr1
| motif2 −> expr2
| ..............
| motifn −> exprn
```

L’ordre dans lequel on essaye de faire correspondre un motif et une valeur a de l’importance :
```ocaml
let sinc = function | x −> sin(x) /. x | 0. −> 1.

Toplevel input :  
> | 0. −> 1. ;;  
> ^^  
Warning : t h i s matching case i s unused . sinc : float −> float = <fun>
```