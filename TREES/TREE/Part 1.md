A tree is a recursive structure:

> A tree is either empty, or it is a node that contains a value and smaller trees below it.

For a binary tree:
	10  
	/ \  
	5 20
Each node has:
	value  
	left subtree  
	right subtree
So the recursive idea is:
	Tree =  
		nothing  
		OR  
		Node(value, leftTree, rightTree)
		
I suggest we start in *OCaml*, because it makes the recursive shape clearest:
```ocaml
type int_tree =  
	| Empty  
	| Node of int * int_tree * int_tree
```
Example tree:
```ocaml
let tree =
  Node (10,
    Node (5, Empty, Empty),
    Node (20, Empty, Empty)
  )
```

First exercises:
1. Count all nodes.
2. Count leaves.
3. Calculate depth.
4. Search for a value.

Try exercise 1:
```ocaml
let rec count_nodes tree =  
match tree with  
| Empty -> ?  
| Node (_, left, right) -> ?
```
The key question: what should `Empty` contribute to the count, and what should a `Node` contribute?


