# Graphs:
***A graph is a non-linear data structure that can be looked at as a collection of vertices potentially connected by line segments named edges.***


### common terminology of a graph:
Vertex - A vertex, also called a node, is a data object that can have zero or more adjacent vertices.
Edge - An edge is a connection between two node.
Neighbor - The neighbors of a node are its adjacent nodes.
Degree - it is a vertex is the number of edges connected to that vertex.
Complete vs Connected vs Disconnected Graphs
Complete Graphs A complete graph is when all nodes are connected .

**Connected is a graph that has all of vertices,nodes have at least one edge.**

**Disconnected is a graph where some vertices may not had edges.**

## Directed vs Undirected:
###### Undirected Graphs((Bigraph)) is a graph where each edge is undirected or bi-directional. This means that the undirected graph doent move in any direction.

###### directed Graphs((Digraph)) is a graph where every edge is directed. Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

## Acyclic vs Cyclic:
***Acyclic Graph is a directed graph without cycles.***
***cycle is when a node can be traversed through and potentially end up back at itself.A directed acyclic graph is also called a DAG.***
***Cyclic Graphs is a graph that has cycles. A cycle is defined as a path of a positive length that starts and ends at the same vertex.***

## Weighted Graphs:
a graph with numbers assigned to its edges. These numbers are called weights.
## Breadth First
In a breadth first traversal, you are starting at a specific node. This node should be specified when calling the BreadthFirst() method. The breadth-first traversal of a graph is like that of the tree, the difference is the graphs can have cycles. When a graph has cycles and we are trying to traverse, this leaves possibility to be in an infinite ,which is bad. To prevent this, we need to had some sort of flag that specifies if we have already visited that vertices. Upon each visit, we just set the “visited” flag from false to true.
## Depth First
In a depth first traversal, we approach it a bit different than the way we do when working with a depth first traversal of a tree. Similar to how the breadth-first uses a queue, we will use a Stack for our depth-first traversal.
The algorithm for a depth first traversal is as follows
Push root node to the stack
Start a while loop while the stack isnt empty
Peek at top node in the stack
If top node has unvisited children, mark top node as visited, and then Push any unvisited children back to the stack.
If top node doent have any unvisited children, pop that node off the stack
repeat until the stack be empty.

# examples of graphs in use
- GPS and Mapping

- Driving Directions

- Social Networks

- Airline Traffic

- Netflix uses graphs for suggestions of products