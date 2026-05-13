Spanning [[Tree]]
A spanning tree is a [[subgraph]] of a G which is a [[Tree]] and contains all the vertices of G. 

An algorithm for producing a spanning tree 
1: Initialise T to be the vertices of G but no edges. Let G have N vertices. 
2: Pick an edge 
3: Add the chosen edge to T IFF it does not make a [[Circuit]] in T 
4: Repeat until T has n-1 edges 