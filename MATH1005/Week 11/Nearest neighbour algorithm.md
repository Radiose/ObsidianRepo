Nearest neighbour algorithm

This is an attempt to solve the travelling salesman problem, IE, find the shortest [[Path]] that can visit n nodes. It should output a [[Hamilton Circuit]] of minimum possible weight. 
We should input a [[weighted graph]]/[[Complete graph]] with n vertices

The algorithm:
 1. Initialise L to the empty list, W to 0 and index i to 1
2. Choose any vertex and append it to L as L(1).
3. From all vertices in G but not in L, choose a vertex v
such that weight(L(i), v ) is as small as possible. (v is a
‘nearest neighbour’ to L(i)).
4. Add weight(L(i), v ) to W . Increment i by 1. Append v
to L as L(i).
5. Repeat steps 3 and 4 until i = n.
6. Add weight(L(n), L(1)) to W . Append L(1) to L as
L(n + 1).

