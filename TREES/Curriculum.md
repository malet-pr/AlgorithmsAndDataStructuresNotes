### Binary tree

##### 1. Construction ✅
- Generic tree
- Example trees
- Records as values
##### 2. Basic recursive queries ✅
- Count nodes
- Count leaves
- Depth
- Search
- find_by
- count_by
##### 3. Traversals
These are the canonical recursive algorithms.
- Preorder
- Inorder
- Postorder
##### 4. Transformations
This is where FP really starts to shine.
- map
- filter
##### 5. Folding (the big one)
This is probably the most important concept. Once you have a tree fold, many of the functions you've already written become special cases of it.
### Binary Search Trees (BST)

Introduce the BST invariant: left < node < right
- validate whether an arbitrary binary tree satisfies the BST invariant
- insert
- search
- minimum
- maximum
- inorder traversal and why it produces sorted output
- delete
    - leaf
    - node with one child
    - node with two children
### N-ary tree

Example:
Project  
	├── API  
	├── DB  
	└── UI  
		├── Components  
		└── Store
Tasks:
- model tree with list of children
- count all nodes
- collect names
- find path to node
- print tree indented
### Extensions

- equality
- pretty printer
- serialization
- iterator
