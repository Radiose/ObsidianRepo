dijkstras algorithm

This is a solution to finding the shortest possible [[Path]] between two vertices. 
The basics of the algorithm are that you utilise a [[Nearest neighbour algorithm]], but at each iteration, you keep track of the shortest distance to the vertex that you want. 
Demonstrating:
Below is a complete connected graph, we aim to find the shorted [[Path]] between vertices A and C
![[Pasted image 20260518180736.png]]

We first label all vertices connected to A with the corresponding distance that they have.

![[Pasted image 20260518180813.png]]

We then select the shortest distance we have and lock it in 
![[Pasted image 20260518181036.png]]

From here, we undergo have three options on a vertex v thats connected to D 
If v is unmarked, we simply add the distance from d to the number on top of d(from A(3))
If v is marked, and is currently less than or equal to the distance from d plus d's number, its unchanged 
if v is marked and is currently greater than the distance from d plus d's number(3), we convert it to the distance from D plus d's number 
![[Pasted image 20260518181437.png]]
We repeat this, and now we lock in E. 
![[Pasted image 20260518181551.png]]
Again, and lock in B

![[Pasted image 20260518181647.png]]

We are now left with the final path. We can trace it backwards. C to B to E to D to A via the labels. 
