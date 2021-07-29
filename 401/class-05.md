# linked list:

A linked list is a data structure in which the objects are arranged in a linear order.
•Unlike an array, though, in which the linear order is determined by the array indices, the order in a linked list is determined by a pointer in each object.
•In the doubly linked lists along the key field there are two pointer fields: prev[x] points to the previous, and next[x] points to the next element of the list.
•If head[L]=NIL, then the list is empty, if next[x]=NIL, then x is the first element of the list, and if prev[x]=NIL, then x is the last element of the list.


## A linked list can be small or huge, but no matter the size, the parts that make it up are actually fairly simple. A linked list is made up of a series of nodes, which are the elements of the list.
The starting point of the list is a reference to the first node, which is referred to as the head. Nearly all linked lists must have a head, because this is effectively the only entry point to the list and all of its elements, and without it, you wouldn’t know where to start! The end of the list isn’t a node, but rather a node that points to null, or an empty value.

***Singly linked lists***: are the simplest type of linked list, based solely on the fact that they only go in one direction. There is a single track that we can traverse the list in; we start at the head node, and traverse from the root until the last node, which will end at an empty null value.

***circular linked list***: is a little odd in that it doesn’t end with a node pointing to a null value. Instead, it has a node that acts as the tail of the list (rather than the conventional head node), and the node after the tail node is the beginning of the list. This organization structure makes it really easy to add something to the end of the list, because you can begin traversing it at the tail node, as the first element and last element point to one another.

***a linked list is usually efficient when it comes to adding and removing most elements, but can be very slow to search and find a single element.***

