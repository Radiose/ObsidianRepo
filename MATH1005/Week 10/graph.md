Graph 
A graph G is a pair comprising of the following 
A set $V(G)$ of vertices, also known as nodes 
A possibly empty [[multiset]] $E(G)$ of edges where the elements are size 2 multisets of vertices

Each edge is specified by a pair of vertices and each edge determines one or two vertices that are its **endpoints**.

In this course, we consider only finite graphs

Note that intersections between edges are generally unimportant unless a vertice is there.

![[Pasted image 20260511153019.png]]

Above is a traditional diagram of a graph. Note that the intersections between db and ac are not relevant. 

## Graph terminology
An **edge** connects its **endpoints**
An **edge** with both **endpoints** is called a **loop**
Two edges may connect the same pair of **endpoints**, in which case they are said to be **parallel** 
Two **vertices** are **adjacent** if they are connected by an edge, two **edges** are **adjacent** if they share an **endpoint**
An edge is an incident on its edge points
A vertex with no incident edges is isolated 
A graph with no vertices is empty 
The **order** of a graph G is the number of vertices in it. 



## Degrees
The degree of a vertex is the number of edges that incident on it. We can determine this by drawing a circle around it, and the number of intersections that are present determines the degree of it.
### Degree of a graph
$\sum_{v \in V(G)} deg(v)$ 
![[Handshake theorem]]

Corollary 
In any [[graph]], there is an even number of vertices of odd degree .
