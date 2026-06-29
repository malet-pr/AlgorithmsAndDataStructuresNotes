### Phase 1 — Mental model

Goal: understand trees as recursive data.

Concepts:

- node
- leaf
- root
- child
- subtree
- depth
- traversal

### Phase 2 — Basic binary tree

Example:
	10  
	/ \  
	5 20

Tasks:

- create tree type/class
- count nodes
- count leaves
- calculate depth
- search for value

### Phase 3 — N-ary tree

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

### Phase 4 — Expression trees

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

### Phase 5 — JSON to tree

This connects directly to the rules project.

Tasks:

- parse JSON into tree
- print tree
- evaluate tree
- handle invalid JSON gracefully

### Phase 6 — Same lab in three languages

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