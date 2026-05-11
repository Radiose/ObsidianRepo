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
