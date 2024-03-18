Pour implémenter une pile en définissant un type récursif en OCaml, nous allons définir un type `pile` qui est soit vide, soit composé d'un élément et d'une référence à une autre pile. Voici comment nous pouvons le faire :

```ocaml
(* Définition du type de pile *)
type 'a pile =
  | Vide (* Cas de la pile vide *)
  | Element of 'a * 'a pile (* Cas d'un élément et d'une référence à une autre pile *)

(* Fonction pour créer une pile vide *)
let creer_pile () : 'a pile =
  Vide

(* Fonction pour empiler un élément sur la pile *)
let empiler (element : 'a) (pile : 'a pile) : 'a pile =
  Element (element, pile)

(* Fonction pour dépiler un élément de la pile *)
let depiler (pile : 'a pile) : ('a * 'a pile) option =
  match pile with
  | Vide -> None (* Si la pile est vide, il n'y a rien à dépiler *)
  | Element (tete, reste) -> Some (tete, reste) (* Retourne la tête de la pile et le reste *)

(* Fonction pour vérifier si la pile est vide *)
let est_vide (pile : 'a pile) : bool =
  pile = Vide

(* Exemple d'utilisation *)
let ma_pile = creer_pile () |> empiler 1 |> empiler 2 |> empiler 3
let est_vide_ma_pile = est_vide ma_pile (* est_vide_ma_pile doit être false *)
let (element, nouvelle_pile) = match depiler ma_pile with
| Some (x, p) -> (x, p)
| None -> failwith "La pile est vide."

```

Dans cette implémentation :

- Le type `pile` est défini de manière récursive. Il peut soit être `Vide`, indiquant une pile vide, soit être `Element` contenant un élément de type `'a` et une référence à une autre pile.
- Les fonctions pour créer une pile vide (`creer_pile`), empiler un élément sur la pile (`empiler`), dépiler un élément de la pile (`depiler`), et vérifier si la pile est vide (`est_vide`) sont implémentées en utilisant le type de pile récursif.
- Nous fournissons également un exemple d'utilisation pour illustrer comment utiliser ces fonctions pour manipuler une pile en OCaml.