## Graphs
Graph:
is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.
Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
Edge - An edge is a connection between two nodes.
Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
Degree - The degree of a vertex is the number of edges connected to that vertex.

# Directed vs Undirected 

### Undirected Graphs

An Undirected Graph is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

### Directed Graphs (Digraph)

A Directed Graph also called a Digraph is a graph where every edge is directed.

Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

## Acyclic vs Cyclic

* An acyclic graph is a directed graph without cycles, a cycle is when a node can be traversed through and potentially end up back at itself.

* A Cyclic graph is a graph that has cycles, a cycle is defined as a path of a positive length that starts and ends at the same vertex.

# Complete vs Connected vs Disconnected 

### Complete Graphs

A complete graph is when all nodes are connected to all other nodes.

### Connected

A connected graph is graph that has all of vertices/nodes have at least one edge.

### Disconnected

A disconnected graph is a graph where some vertices may not have edges.


## Graph Representation
Adjacency Matrix
An Adjacency matrix is represented through a 2-dimensional array.

 If there are n vertices, then we are looking at an n x n Boolean matrix Each Row and column represents each vertex of the data structure.


The elements of both the column and the row must add up to 1 if there is an edge that connects the two, or zero if there isn’t a connection.


Adjacency List
An adjacency list is the most common way to represent graphs.

An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.

Adjacency lists make it easy to view if one vertices connects to another.

## Traversals
BreadthFirst: You start at a specific node. We need to create a visited set to keep track of nodes we have already traversed and to prevent going into cycles, causing infinite loop.

Actual breadth first traversal definition: when you visit all nodes closest to the root, then keep traversing level by level.

Breadth first algo:
```

Enqueue the declared start node into the Queue.
Create a loop that will run while the node still has nodes present.
Dequeue the first node from the queue
if the Dequeue‘d node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.
```
Pseudo code for breadth first:
```
ALGORITHM BreadthFirst(vertex)
  DECLARE nodes <-- new List()
  DECLARE breadth <-- new Queue()
  DECLARE visited <-- new Set()

  breadth.Enqueue(vertex)
  visited.Add(vertex)

  while (breadth is not empty)
      DECLARE front <-- breadth.Dequeue()
      nodes.Add(front)

      for each child in front.Children
          if(child is not visited)
              visited.Add(child)
              breadth.Enqueue(child)   

  return nodes;

```
Depth first traversal algo:
```
Push the root node into the stack
Start a while loop while the stack is not empty
Peek at the top node in the stack
If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.
If the top node does not have any unvisited children, Pop that node off the stack
repeat until the stack is empty.
```
Real word uses for graphs:

* GPS and Mapping
* Driving Directions
* Social Networks
* Airline Traffic
* Netflix uses graphs for 
* suggestions of products

## Resources

[sohttps://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)urces1](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)