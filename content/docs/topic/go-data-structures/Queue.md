# Go Data Structures

Code and explanation of a Go data structure

## Queue

First we look at the queue data structure. A queue is a simple list where we add to the back and remove from the front. Below is the class structure of the list in Go, creating a Node - when initiated keeps track of it’s head, tail and the next element in the list.

```tpl
// Queue : holds 2 nodes
type Queue struct {
	Head *Node
	Tail *Node
}

// Node : A Queue node
type Node struct {
	Next *Node
	Data interface{}
}

// New : Create a new Queue
func New() *Queue {
	emptyNode := &Node{
		Next: nil,
		Data: nil,
	}
	return &Queue {
		Head: emptyNode,
		Tail: emptyNode,
	}
}
```

## Enqueue and Dequeue

Algorithms for popping off the front and adding to the back, using a linked list.

```tpl
// Appends to the end of the list
func (q *Queue) Enqueue(d interface {}) *Queue {
    nextNode := &Node {
        Next: nil,
        Data: d,
    }
    if q.Head.Data == nil {
        q.Head = nextNode
    } else {
        q.Tail = nextNode
    }
    q.Tail = nextNode
    return q
}

func (q *Queue) Dequeue() *Queue {
    var node = q.Head
    q.Head = q.Head.Next
    
    return q
}

```
{{< button href="https://github.com/trmchale1/go_datastructures/blob/main/go_data_structures/queue/queue.go" >}}Code{{< /button >}}
