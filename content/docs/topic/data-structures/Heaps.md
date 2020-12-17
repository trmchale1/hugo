# Data  Structures 

Psuedo-code and explanation for a Data Structure, based upon CLRS

## Heaps

Heaps are useful as an n log n sorting algorithm, that can also be used as a priority queue. It is a useful data structure that can maintain its structure with calls to heapify.

## Heap Indexes 

Heaps and Trees in general follow these rules

```tpl
Parent(i)
return(|i/2|)

Left(i)
return 2i

Rigtht(return 2i+1)
```

## Max-Heapify

This operation checks the children of a node to see if they are larger than their parent. If large the node moves up the tree.

```tpl
Max-Heapify(A,i)
l = left(i)
r = right(i)
if l <= A.heap-size and A[l] > A[i]
    largest = l
else 
    largest = i
if r <= A.heap-size and A[r] > A[largest]
    largest = r
if largest != i
    exchange A[i] with A[largest]
    Max-Heapify(A,largest)
```


