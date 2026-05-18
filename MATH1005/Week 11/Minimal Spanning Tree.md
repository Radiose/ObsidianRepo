---
aliases:
  - kruskal's algorithm
---
Minimal [[Spanning Tree]]
This algorithm is a modification to the original spanning tree algorithm laid out in the spanning tree note. 
The basic idea: Will adding this edge make a non trivial [[Circuit]]? 
The extension: We use the edge that has the lowest weight. Will adding this weight create a non trivial [[Circuit]]? If it will, try the next smallest weight. 

The algorithm we implement: 
1. Initialise T to have all the vertices of G but no edges.
Initialise W to 0.
2. From the edges of currently in G pick one, e, of least
weight and remove it from G .
3. If adding e to T does not create a circuit in T , add e
to T and add weight(e) to W .
4. Repeat steps 2 and 3 until T has n − 1 edges


The images below demonstrate the entire algorithm 

![[Pasted image 20260518171818.png]]

![[Pasted image 20260518171830.png]]