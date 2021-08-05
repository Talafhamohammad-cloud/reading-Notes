# Stack:

A stack is a data structure which implements a LIFO policy, i.e. the element deleted from the stack is the one most recently inserted
The INSERT operation on a stack is often called Push, and the DELETE operation, is often called Pop
We can implement a stack of at most n elements with an array S[1…n], where top[S] is the most recently inserted element, the stack cosists of elements S[1…top[S]], wehre V[1] is the elemt at the bottom and, S[top[S]] is the element at the top.
If top[V]=0 then the stack is empty.

# queue:

The queue is a data structure which implements the FIFO policy, i.e. the deleted element is the one which is in the queue for the longest time
We call the INSERT operation on a queue ENQUEUE, and the DELETE operation DEQUEUE. The index of the first element is head[Q], the index of the next inserted element is tail[Q].
The elements in the queue are in the locations head[Q], head[Q]+1,…, tail[Q]-1, and the queue is empty if head[Q]=tail[Q]. Initially we have head[Q]=tail[Q]=1. If head[Q]=tail[Q]+1 then the queue is full.

# Algorithm:

## ALOGORITHM push(value)

INPUT <-- value to add, wrapped in Node internally
OUTPUT <-- none
node = new Node(value)
node.next <-- Top
top <-- Node

## ALGORITHM pop()

INPUT <-- No input
OUTPUT <-- value of top Node in stack
EXCEPTION if stack is empty

Node temp <-- top
top <-- top.next
temp.next <-- null
return temp.value

## ALGORITHM peek()

INPUT <-- none
OUTPUT <-- value of top Node in stack
EXCEPTION if stack is empty

return top.value

## ALGORITHM isEmpty()

// INPUT <-- none
// OUTPUT <-- boolean

return top = NULL

## ALGORITHM enqueue(value)

// INPUT <-- value to add to queue (will be wrapped in Node internally)
// OUTPUT <-- none
node = new Node(value)
rear.next <-- node
rear <-- node

## ALGORITHM dequeue()

// INPUT <-- none
// OUTPUT <-- value of the removed Node
// EXCEPTION if queue is empty

Node temp <-- front
front <-- front.next
temp.next <-- null

return temp.value

## ALGORITHM peek()

// INPUT <-- none
// OUTPUT <-- value of the front Node in Queue
// EXCEPTION if Queue is empty

return front.value

## ALGORITHM isEmpty()

// INPUT <-- none
// OUTPUT <-- boolean

return front = NULL
