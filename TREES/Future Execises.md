There’s one useful binary-tree exercise left that fits beautifully into a single session: **paths**.

### Your 60–90 minute exercise

Add a function that finds the path from the root to a requested value.

For example, given conceptually:

```
        8
       / \
      3   10
     / \
    1   6
```

you should be able to ask for `6` and obtain something representing:

```
8 -> 3 -> 6
```

You decide the OCaml API yourself: return type, whether the path is root-first or target-first, and how you represent “not found.” Don’t optimize prematurely; the point is recursion and tree structure.

**Coding deliverable:** implement the path-finding function in your existing binary-tree module without changing the tree type.

**Alcotest:** keep it tiny. Write one test for a value several levels down, checking the complete path, and one test for a missing value. If you finish early, add the root itself as a trivial edge case.

There’s a nice constraint for you: **do not use your existing `find_value` as a preliminary search.** Let the recursive path algorithm discover whether the element exists. Otherwise you end up walking the tree twice.

---

Can't I traverse the tree by wo_number and, in case I find it compare the class?

Yes — absolutely. And in your domain, that is probably the more sensible design.

If `wo_number` is unique and is the BST key, you can:

1. traverse the BST using only `wo_number`
2. when you find the matching node, then check `wo_class`
3. return true/false or the record depending on what you want

So the tree navigation still uses the one field that actually defines the ordering.

Conceptually:

```
compare target.wo_number current.wo_number
→ choose left/right

if numbers match
→ now inspect wo_class too
```

That is different from making `wo_class` part of the comparator.

And because `wo_number` is unique, once you find that number, there is no need to keep searching elsewhere. You have found the only possible candidate.

So yes: you can have something like a more specific query:

```
find WO where
number = 100
and class = Event
```

while still storing/ordering the BST only by number.

That’s actually a nice distinction:

```
ordering key: wo_number
matching criteria after lookup: wo_number + wo_class
```

Much cleaner than inventing an artificial total order over `class_variant`.
