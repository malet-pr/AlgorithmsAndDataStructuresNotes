Absolutely. And I actually think a recall session is the right way to restart instead of jumping straight into new material.

From what I remember, you finished a surprisingly complete OCaml binary tree library:

- Generic `'a b_tree`
- Recursive algorithms (`count_nodes`, `count_leaves`, `calculate_depth`)
- `find_value`, `find_by`, `count_by`
- Traversals (`preorder`, `inorder`, `postorder`, plus a generic `order`)
- `map`
- `.mli` files
- Alcotest
- Parameterized tests
- Test fixtures and test cases split into separate modules
- Everything green on Clementina. 😊

Let's spend about 20 minutes getting your tree brain back.

---

## Exercise 1 – Types (no coding)

Without looking at your code, tell me the type signatures of these functions.

```ocaml
count_nodes

val count_nodes : 'a b_tree -> int
```

```ocaml
find_by

val find_by : ('a -> bool) -> 'a b_tree -> bool
```

```ocaml
map

val map : ('a -> 'b) -> 'a b_tree -> 'b b_tree
```

Don't worry about exact spacing; I want to see whether you remember the ideas.

---

## Exercise 2 – Trace recursion

Suppose we have

```
      8
     / \
    3   10
```

Walk me through the recursive calls of

```text
count_nodes
```
I don't need every line, just the order in which the recursion visits the nodes.
1) count the first node (value: 8, count = 1)
2) add the result of applying the function to the left tree and the right tree (left node: 3 and right node: 10, count = 3)

---

## Exercise 3 – Traversals

For

```
        10
       /  \
      5    20
     / \   / \
    7   9 12 15
```

Give me:

- preorder: 10,5,7,9,20,12,15
- inorder: 7,5,9,10,12,20,15
- postorder: 7,9,5,12,15,20,10

No peeking. 😄

---

## Exercise 4 – Generic thinking

Suppose you have

```
type person =
{
  name : string;
  age : int;
}
```

and a

```
person b_tree
```

Could you use

```
count_nodes
```

without changing it? Yes

Why? As I defined count_nodes it takes a generic type 'a for the tree, so it should work.

---

## Exercise 5 – A tiny implementation

Complete this from memory:

```
let rec map f tree =
  match tree with
  | Empty -> Empty
  | BNode (v, left, right) ->
      BNode (f v, map f left, map f right)
```

---