# Data Structures

Psuedo-code and explanation for a Data Structure, based upon CLRS

## Stack

A stack is a fundamental data structure. It is used in the Operating System, memory is implemented as a stack. If we are able to visualize a stack, it will help us visualize some of the more complex ideas in computer science.


### Stack Operations

The Stack has the following operations: it must keep track of the top of the Stack, it must know if the Stack is empty, also the Stack must be able to perform push pop operations. The Stack inserts new data by pushing it on the top of the Stack. The Stack deletes by pushing the top member off of the Stack 

```tpl
Stack-Empty(S)
if D.top == NULL
    return TRUE
else
    FALSE

Push(S,x)
S.top = S.top + 1
S[S.top] = x

Pop(S)
if Stack-Empty(S)
    error 'underflow'
else
    S.top = S.top - 1
    return S[S.top + 1]
```

