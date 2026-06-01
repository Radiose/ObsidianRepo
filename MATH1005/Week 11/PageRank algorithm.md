
## Webgraph
A webgraph described the directed links between pages of the world wide web. it is a form of [[directed graph|digraph]].
A directed link is one that connects page x to page y provided a hyperlink exists on page x referring to page y.

# PageRank
This is a link analysis algorithm that assigns a numerical value to each element of a hyperlinked [[set]] of documents with the purpose of measuring its relative importance. 

The fundamentals
The number of links pointing at a page is important
The no of linked pointing to those vertices linking to a page is important 

The importance of a page j is defined is $p_{j}$ in the [[Steady state vector]] S for a [[Random walk on a graph|random walk]] on a webgraph using a specially designed [[Transition Matrix]].

### The basics 
A random surfer, or walker, moves around the web as follows 
At any page, the surfer is equally likely to follow any link on a page, and if there are no links, to teleport to a random page. 

Formally, for any webgraph G we construct $G^+$ by adding edges by adding to edges from any
vertex that has no links to all other vertices (we remove the sinks). Let $n$ be the
number of vertices (pages) and for each vertex $i$ let $n_{i}$ be the number vertices to
which $i$ is adjacent in $G^+$, that is
$n = |V(G)|$
$n_{i}=|\{ j:(i,j) \in E(G) \}|$
Then the basic probability of moving from vertex $j$ to $i$ is given by
$p_{ij} = \{\frac{1}{n_{j}}$ if $n_{j}=0$ and $(j, i) \in E$ 
	 $\{  0$ otherwise
The basic [[Transition Matrix]] is $T = (p_{i,j})_{1 \le i,j \le n}$


## The damping factor 

This is an additional factor of randomness implemented into the [[Random walk on a graph|random walk]]. 
There is a small chance that the surfer acts as if there are no links from the page, and instead will teleport randomly to another page/vertex. 

For convenience, we include the current page amongst the possibilities for this
random choice, so that the probability that the surfer takes the teleport option
and lands on any particular page is $\alpha\left( \frac{1}{n} \right) = \frac{\alpha}{n}$

Correspondingly, at any time $k$, the probability that the surfer takes the standard
‘non-teleport’ option is$(1 − \alpha)$, thus reducing the basic probabilities $p_{i,j}$ by a
**damping factor**  $(1 − \alpha)$.
Thus the modified probability for transition from vertex $j$ to $i$ is
$m_{i,j}= α/n + (1 − α)p_{i,j}$

Google typically uses a damping factor of $(1-\alpha)=0.85$
The total matrix is $M = (α/n)U + (1 − α)T$, where U is the $n\times n$ matrix of ones

## Iterative method 
When n is huge, as it is with the WWW, solving the n × n linear system
$(M − I )PR = 0$becomes computationally infeasible.

A  simpler method starts from the defining equation attempts to
find $PR$ by iteratively calculating the chain of probability vectors$P_{0}, P_{1},\dots$ where
$P_{0}$ is arbitrary and $P_{k} = MP_{k-1}$ for $k ≥ 1$ (so  $P_{k} = M^k P_{0}$).

A steady state is reached when $P_{k} ≈ P_{k−1}$. Then declare that $PR ≈ P_{k}$ .

Now $Pk = MP_{k−1}$
$= [(α/n)U + (1 − α)T ]\ P_{k−1}$
$= (α/n)1 + (1 − α)TP_{k−1}$
where 1 is a column of 1's. Its natural to start with all ranks equal. So, the iterative scheme is 
$P_{0} = (1/n)1; P_{k} = αP_{0} + (1 − α)TP_{k−1}, k ≥ 1$
So, the first initial vector is just evenly spread between the number of webpages, so 4 pages results in $p_{0}$ looking like 0.25 


