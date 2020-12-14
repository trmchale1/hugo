# Python Data Structures

Code and explanation for a Python Data Structure

## Stack

A stack is a fundamental data structure. It is used in the Operating System, memory is implemented as a stack. If we are able to visualize a stack, it will help us visualize some of the more complex ideas in computer science.

Below the python class structure for a Stack.

```tpl
class Stack:
    class _Node:
        __slots__ = 'element', 'next'

        def __init__(self,element, next):
            self._element = element
            self._next = next

        def __init__(self):
            self._head = None
            self._size = 0
```

### Pushing onto and Popping off of the Stack

Algorithms for pushing onto and popping off of the Stack, using a linked list. 

```tpl
    def push(self,e):
            self._head = self._Node(e,self._head)
            self._size += 1

    def pop(self):
            if self.is_empty():
                raise Empty('Stack is empty')
            answer = self._head._element
            self._head = self._head._next
            self._size -= 1
            return answer
```

### Links

Code with the full program and helper methods below

{{< button href="https://github.com/trmchale1/py_algos/blob/main/stack.py" >}}Code{{< /button >}}
