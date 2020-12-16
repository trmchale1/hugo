# Python Data Structures

Code and explanation for a Python Data Structure

## Trees

Trees provide a natural organization for data, and are used in file systems, websites and GUIs. It is an abstract data type that stores elements hierarchically, each element has a parent and one or more children.  

## Tree Traversals

A traversal is a way of accessing or visiting all the positions in a tree

Preorder traversal, where the children of each position are ordered from left to right

```tpl
Algorithm preorder(tree, position)
    visit p
    for each child in tree.children(p) do
        preorder(tree,child)
```

Postorder traversal, where the algorithm recursively traverses the the leaves first

```tpl
Algorithm postorder(tree,position)
    for each child c in T.children(p) do
        postorder(tree,child)
```

Inorder traversal, starts left and goes up the tree before going right

```tpl
Algorithm inorder(p):
    if p has a left child lc then
        inorder(lc)
    perform the "visit" action for position p
    if p has a right  child rc then
        inorder (rc)
```

