- Statement: A sentence that is **either** true or false, but not both.
- Compound statements: built using [[logical connective]]s
- P is a sufficient condition for Q means $p \implies q$
- P is a necessary condition for Q means $\neg p \implies \neg q$
- Predicate: a sentence containing one or more variables with the property that, when a value from a specified domain is given to each variable, the sentence becomes a [[Statement]]. The specified domain is the domain of the predicate.




- Pairwise disjoint: Two [[set]]s are **disjoint** when $a \cap B = \emptyset$. This means that there are no elements in both sets. 
	Given a set of sets $\mathcal{S}$, the sets in S are said to be in pairwise disjoint when 
	$\forall a,b \subset S | a\not=b$ and $a \cap b = \emptyset$
- Axiom of extensionality: A [set](app://obsidian.md/set) is defined solely by the elements that comprise it .                     
	No importance is given to order or frequency of elements

-  A is a **partition** of S when each of the following are true:
	1: $\emptyset \not\in A$
	2: every element of S is an element of some set in A. 
	ie $\forall s \in S, \ \  \exists A \in A$   $s\in A$. Think about this as: a partition is a set of sets, with its elements ([[set]]s) being also sets in S ([[powerset]]s).
	3: The sets in A are pairwise disjoint
	
- subsets $a \subset b \iff \forall x(x\in a \implies x\in b)$

- Given (not necessarily distinct) sets $A_{1}$, $A_{2}$, . . . , $A_{n}$, the Cartesian
	product of $A_{1}, A_{2}$, . . . , $A_{n}$, denoted $A_{1} × A_{2} × · · · × A_{n}$, is the set of all
	ordered n-tuples ($a_{1}, a_{2}, . . . , a_{n}$) where $a_{1}$ ∈ $A_{1}$, $a_{2} ∈ A_{2}$, . . . ,$a_{n} ∈ A_{n}.$


- relation: let A,B be non empty [[set]]s. Any [[subset]] of AxB is called a relation from A to B. A relation from A to A is called a relation on A. A [[Cartesian product]]s subset is a relation

- $r^{-1}=\{ (b,a)\in B\times A|(a,b) \in R \}$
	the inverse relation $r^{-1}\subset B\times A$
	thus $b R^{-1}a \iff a Rb$

- reflexive [[relation]]
	Let S be a set and let ~ be a relation on S. We say that
	~ is reflexive when $\forall s \in S s$ ~$s$ 
	This means every element is related to itself. The less than relation is not reflexive. The less than or equal to relation on the set of integers is reflexive.

- symmetric [[relation]]
	~ is symmetric when $\forall s,\ t \in S\ s$~$t \to t$~$s$ 
	This means every element of s is related to t, and that t is related to s.
	The less than or equal to is not symmetric. 6 is less than or equal to 7, but 7 is not less than or equal to 6.

- an equivalence relation is a [[reflexive relation]], [[transitive relation]] [[symmetric relation]]. This means that it could serve as your idea of somethings being the same.

- We say that the [[relation]] is antisymmetric when $\forall s,t \in S((s \textasciitilde t)\land (t \textasciitilde s) \to s = t)$

- Partial order If ~ is a [[reflexive relation]], a [[transitive relation]] and asymmetric, then we say that ~ is a partial order on s.




- Function: 
	- let A,B be sets. A [[relation]] F from A to B is called a function from A to B when $\forall a \in A \exists!b\in B (a,b) \in f$

- injective: $\forall a_{1},a_{2} \in A(a_{1} \not=a_{2}) \implies f(a_{1})\not=f(a_{2})$
- surjective  $\forall b \in B \exists a \in A f(a)=b$.
- bijection - injective and surjective OR $∀y∈B, ∃!x∈A, f(x)=y$





the quotient remainder [[theorem]]
$\forall z \in \mathbb{Z} \forall d \in \mathbb{N} \exists!q \in \mathbb{Z}\exists!r \in \mathbb{Z}(z = qd+r)\land(0 \le r \le d)$ 
Basically, for all integers, there exists a quotient, a divider and a remainder such that the remainder is less than the divisors. 

A digit in base 2 is called a bit
a block of 8 bits is called a byte
a block of 4 bits is called a nibble
a sequence of several adjacent **bytes** is called a word. The number of bytes varies, depending on the purpose of the word. For example, a 2 byte word can store non negative integers in the range from 0 to $2^{16}-1$.



$P:S→\mathbb{Q}^+$  $X:S→\mathbb{Q}$
The random variable maps an element in the sample space to an outcome. For example, this job maps to this life outcome.


For a [[Sample space]] S with probability [[Density function]] P. $E,F \in \mathcal{P}(S)$ are called *independent* events when $\mathbb{P}(E \cap F)=\mathbb{P}(E)\times \mathbb{P}(F)$



If k + 1 or more pigeons occupy K pigeonholes occupy K pigeonholes, then at least one pigeonhole must contain two or more pigeons. 

Generalised pigeonhole principle
If N objects are classified in K disjoint categories, then at least one category must contain $[\frac{n}{k}]$ objects, where  $[\frac{n}{k}]$  means the least integer that is greater than or equal to $\frac{n}{k}$



graphs: 



- A graph G is a pair comprising of the following : 1: A set $V(G)$ of vertices, also known as nodes
	 2: A possibly empty [[multiset]] $E(G)$ of edges where the elements are size 2 multisets of vertices

- The degree of a vertex is the number of edges that incident on it. We can determine this by drawing a circle around it, and the number of intersections that are present determines the degree of it.

- Handshake theorem 
	 Handshake [theorem](app://obsidian.md/theorem)  
	 If G is any [graph](app://obsidian.md/graph), then the total degree of G equals twice the number of edges of G   
	 This is because when we count degrees we are counting edges, but we count both ends of each edge, hence we count all the edges twice. 
	- Corollary  In any [graph](app://obsidian.md/graph), there is an even number of vertices of odd degree .


- Adjacent vertices  
	U,V are adjacent if . They are basically adjacent if they have an edge between them.

- Isomorphism 
	An isomorphism between two [[graph]]s $G_{1} \ \text{and } G_{2}$ is a [[Bijective|bijection]] 
	$f: G_{1}(V_{1}) \to G_{2}(V_{2})$ such that $(u,v)$ is an edge in $E(G_{1})$ exactly as many times as $(f(u),f(v))$ is an edge in $E(G_{2})$
	This mapping must preserve multiplicity of edges and non edges.
	If an isomorphism exists between two graphs, we say that they are **isomorphic**.



Every [[Connected graph]] has a [[Spanning Tree]]
Any two [[Spanning Tree]]s for a graph have the same number of edges




Mistakes: 
Probability:
x OR y - likely exlusive or - remember to subtract p(x^y)
Estimate vs exact - makes difference between independence of two random variables 



Counting the number of subgraphs

Don’t forget that every set has itself and the empty set as subsets.

The number of subgraphs of a completed graph can be determined by fixing the number of vertices and counting the amount of possible edges 
logic has to follow these conventions:
First, determine the total amount of edges present. 
Then, we determine the total amount of graphs that could be present for each amount of vertices 
For example, $k_{4}$ has 6 edges 
In the case of 4 vertices, 
$\begin{pmatrix}4  \\ 4\end{pmatrix}\cdot {2}^6$ - the choose function is the number of ways you can combine the vertices, and the $2^6$ is the formula for the [[powerset]] of the edges. 
$+ \begin{pmatrix}4  \\ 3\end{pmatrix} \cdot 2^3$ - we note that for each size 3 subgraph, there are at most 3 vertices, and a similar story happens, where we get the powerset of that graph  
$+ \begin{pmatrix}4  \\ 2\end{pmatrix} \cdot 2^1$ - there is at most one edge. 
$+ \begin{pmatrix}4  \\ 1\end{pmatrix}$ - there are no possible edges 
$+ 1$ - for empty set 
 sum these together for the final answer 



More graph counting: 
Number of edges in a [[Complete graph]]: $\begin{pmatrix}n  \\ 2\end{pmatrix}$
The amount of possible ways edges can be arranged with n vertices $2^{\begin{pmatrix}n  \\ 2\end{pmatrix}}$

A very important thing about counting: 
We are literally counting. For example, the amount of complete graphs with one node removed is the same as the amount of ways to remove one node from a complete graph. 