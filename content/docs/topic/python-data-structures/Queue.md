# Python Data Structures

Code and explanation for a Python Data Structure

## Queue

First we look at the queue data structure. A queue is a simple list where we add to the back and remove from the front. Below is the class structure of the list in python, creating a Node - when initiated keeps track of it's head, tail and the next element in the list.

```tpl
class _Node:
    __slots__ = '_element', '_next'

    # Constructor 
    def __init__(self):
        self._head = None
        self.tail = None
        self._next = next
```

### Enqueue and Dequeue

Algorithms for popping off the front and adding to the back, using a linked list. 

```tpl
def dequeue(self):
        if self.is_empty():
            raiseEmpty('Queue is empty')
        answer = self._head._next
        self._size -= 1
        if self.is_empty():
            self._tail = None
        return answer

    def enqueue(self):
        newest = self._Node(e,None)
        if self.is_empty():
            self._head = newest
        else:
            self._tail._next = newest
        self._tail = newest
        self._size += 1
```

### Links

Code with the full program and helper methods below

{{< button href="https://github.com/trmchale1/py_algos/blob/main/queue.py" >}}Code{{< /button >}}
