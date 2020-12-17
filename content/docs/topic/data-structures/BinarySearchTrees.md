# Data Structures

Psuedo-code and explanation for a Data Structure, based upon CLRS

## Binary Search Trees

Search Tree supports dynamic set operations, including Search, Minimum, Maximum, Predecessor, Successor, Insert and Delete

As you can see we use recursive algorithms for these operations

```tpl
Inorder-Tree-Walk(x)
if x != NIL
    Inorder-Tree-Walk(x.left)
    print x.key
    Inorder-Tree-Walk(x.right)
```

```tpl
Tree-Search(x,k)
if x == NIL or k === x.key
    return x
if k < x.key
    return Tree-Search(x.left,k)
else
    return Tree-Search(x.right,k)
```

## Insertion and Deletion

Modifying the tree to insert a new element is straight forward, but deletions are more intricate

```tpl
Tree-Insert(T,z)
y = NIL
x = T.root
while x != NIL
    y = x
    if z.key < x.key
        x = x.left
    else 
        c = c.right
z.p = y
if y == NIL
    T.root = z
else if 
    z.key < y.key
    y.left = z
else 
    y.right = z
```

In order to move subtrees around within the binary search tree, we define a subroutine Transplant which replaces one subtree as a child of its parent with another subtree.

```tpl
Transplant(T,u,v)
if u.p == NIL
    T.root = v
else if u == u.p.left
    u.p.left = v
else
    u.p.right = v
if v != NIL
    v.p = u.p

Delete(T,z)
if z.left == NIL
    Translpant(T,z,z.right)
else if z.right == NIL
    Transplant(T,z,z.left)
else
    y = Tree-Min(z.right)
if y.p != z
    Transplant(T,y,y.right)
    y.right = z.right
    y.right.p = y
Transplant(T,z,y)
y.left = z.left
y.left.p = y
```


