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
5. Count occurrencies.

#### Traversals
Implement pre- in- and postorder
- **Pre**-order → visit the node **before** its children.
- **In**-order → visit the node **in between** the two subtrees.
- **Post**-order → visit the node **after** its children.

```text
     10  
    /  \  
  5    20
 / \   / \
7   9 12  15

preorder: 10,5,7,9,20,12,15
inorder: 7,5,9,10,12,20,15
postorder: 7,9,5,12,15,20,10
```

---

I'd like to end with a challenge instead of giving you the implementation.
You'll already know how to visit every node. I'll ask:

> "Can you write one generic function that describes _how_ to visit a tree, and express all three traversals using it?"

Don't worry if we don't solve it today. It's a nice bridge toward `fold`, which is one of the most elegant abstractions in functional programming.
