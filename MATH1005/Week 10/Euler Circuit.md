Euler [[Circuit]]
A circuit that passes through every edge
A euler circuit exists IFF each of its vertices have an odd degree 

We have a simple algorithm for locating [[Euler Circuit]]s
As we cross an edge, we mark it as used/remove it
Dont cross an edge unless you have to
When crossing an edge, ensure that the reduced graph is still a [[Connected graph]].
Always leave an edge to return to the start vertex as the last step.
