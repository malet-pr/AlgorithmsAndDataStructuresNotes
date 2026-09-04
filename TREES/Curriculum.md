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
##### 6. Binary Search Trees (BST)
Introduce the BST invariant: left < node < right
- insert
- search
- minimum
- maximum
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

### Expression trees

Example:
	And  
	├── Atom A  
	└── Or  
		├── Atom B  
		└── Atom C

Tasks:

- evaluate boolean tree
- simplify tree
- collect atoms
- compare binary vs n-ary design

### JSON to tree

This connects directly to the rules project.

Tasks:

- parse JSON into tree
- print tree
- evaluate tree
- handle invalid JSON gracefully

### Same lab in three languages

For each concept:
1. Explain concept  
2. Implement in OCaml  
3. Implement in Java  
4. Implement in Python  
5. Compare styles

This is especially useful because each language teaches a different lesson:
- OCaml -> recursive types + pattern matching  
- Java -> classes/sealed interfaces + explicit structure  
- Python -> lightweight modeling + quick experimentation