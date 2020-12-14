# Go Data Structures

Code and explanation for a Go Data Structure

## Stack

A stack is a fundamental data structure. It is used in the Operating System, memory is implemented as a stack. If we are able to visualize a stack, it will help us visualize some of the more complex ideas in computer science.

Below the Go class structure for a Stack.

```tpl
type Stack struct {
    Head *Node
    int size = 0
}

type Node struct {
    Next *Node
    Data interface{}
}

func New() *Stack {
    emptyNode := &Node{
        Next: nil,
        Data: nil,
    }

    return &Stack{
        Head: emptyNode,
        size: 0,
    }
}
```

### Pushing onto and Popping off of the Stack

Algorithms for pushing onto and popping off of the Stack, using a linked list. 

```tpl
func (s *Stack) Push(d interface{}) *Stack {
    nextNode := &Node{
        Next: nil,
        Data: d,
    }
    if s.Head.Data == nil {
        s.Head = nextNode
        s.size += 1
    } else {
       s.Head.Next = s.Head
       s.Head = nextNode
       s.size += 1
    }
    return s
}

func (s *Stack) Pop(v interface{}) *Stack {
    if s.IsEmpty() == true {
        fmt.Println("Stack is empty")
        return s
    }
    var node = s.Head
    s.Head = s.Head.Next
    s.size -= 1
    return s
}
```

### Links

Code with the full program and helper methods below

{{< button href="https://github.com/trmchale1/go_datastructures/blob/main/go_data_structures/stack/stack.go" >}}Code{{< /button >}}
