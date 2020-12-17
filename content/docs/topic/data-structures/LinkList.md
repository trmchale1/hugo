# Data Structures

Psuedo-code and explanation for a Data Structure, based upon CLRS

## Linked Lists

A data structure where objects are arranged in linear order. Unlike an array a pointer must point to the next location in memory.

## List Search

Loop until our key matches

```tpl
List-Search(L,k)
while != nil and x.key !=k
    x = x.next
return x
```

## List Insert

We would have to perform a list search first

```tpl
List-Insert(L,x)
x.next = L.head
    L.head.prev = x
L.head = x
x.prev = NIL
```
## List Delete

We would also need to search for the element by its key before we can delete it

```tpl
List-Delete(L,x)
if x.prev != NIL
    x.prev.next = x.next
else
    L.head = x.next
if x.next != NIL
    x.next.prev = x.prev
```
