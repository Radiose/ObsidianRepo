---
aliases:
  - random walk
---
Random walks on a [[graph]]
# Idea
The idea with a random walk revolves around predictions.
let G be a [[directed graph|digraph]] with n vertices. V = V(G) = $\{ 1,2\dots,n \}$ and directed edge [[set]] E = E(G)

Imagine that you are walking on this digraph. Travelling through edges takes one unit of time.
At time 0, you are at vertex x
At time 1, you are at vertex y $\in V$ with $(x,y) \in E$
At time 2, you are at vertex $z \in V$ with $(y,z) \in E$]
At time k, you are a vertex t and there is a [[Walk]] from x to t
Before each step, you choose where to go probabilistically. The probability of moving from j to i is $P_{i,j}$, note that if $(i,j) \not\in E \implies P_{i,j}=0$

# Formal definition
Associated to an $n$ vertex [[directed graph]] G, let $T = (p_{i,j})_{1\le i,j\le n}$ be a [[Matrix]] such that $p_{i,j}=0 \forall(j,i) \not\in E(G)$

For any given $n$ let $B_{n}$ denote the set of [[Basis]] [[vector]]s, where $e_{i}$ is the n x 1 vector with 1 as the $i$-th entry and all other entries 0.

For $X_{0}=e_{i} \in B_{n}$, the [[Markov process|Markov]] chain  $(X_{k})_{k \in \mathbb{N^+}}$ specified by G and T is called the [[Random walk on a graph|random walk]] on G starting at vertex $i$, with [[Transition Matrix]] T.

Then $X_{k}=T^ke_{i}=(q_{j})_{1 \le j \le n}$, the [[Probability of an event|probability]] of $q_{j}$ of being at the vertex $j$ after $k$ steps starting from vertex *i*.

something important to remember: The [[Adjacent vertices|adjacency matrix]] is from row to column, while we treat the [[Transition Matrix]] as column to row.

