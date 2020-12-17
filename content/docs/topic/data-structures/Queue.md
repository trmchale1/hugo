# Data Structures

Psuedo-code and explanation for a Data Structure, based upon CLRS

## Queue

A queue is a data structure where we keep track of the head and tail. New elements enqueue on the tail and dequeue from the head.

```tpl
Enqueue(Q,x)
Q[Q.tail] = x
if [Q.tail] == Q.length
    Q.tail = 1
else 
    Q.tail = Q.tail + 1

Dequeue(Q)
    x[Q.head]
    if Q.head == Q.length
        Q.head = 1
    else 
        Q.head = Q.head + 1
        return x
```

