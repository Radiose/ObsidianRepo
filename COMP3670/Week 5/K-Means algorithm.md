Input $\mathcal{D}=\{ \mathbf{x_{1}},\dots,\mathbf{x_{n}} \}\subset \mathbb{R}^d$ and a [[partition]] into $k \geq {2}$ nonempty clusters. 

We compute the [[centroid]] $\mathbf{c}_{r}$ of each cluster $\mathcal{C}_{r}$
We then assign each $\mathbf{x_{i}}$ to a [[clustering|cluster]] who's [[centroid]] is closest.
If tied, we retain the current cluster. 
Then, we repeat until no cluster changes. 


# The objective 
The goal of the K-means algorithm is to minimise the within cluster **sum of squared error**

Formally:
For nonempty clusters with centroids $\mathbf{c_{1}},\dots,\mathbf{c}_{k}$, the within cluster sum of squared errors is $$J(\mathbf{C}_{1},\dots,\mathcal{C}_{k})=\sum_{r=1}^k \sum_{\mathbf{x}_{i}\in \mathcal{C}_{r}}||\mathbf{x_{i}-\mathbf{c}}||_{2}^2$$
We seek some partition with small SSE.


The point is that increasing SSE is impossible with the K-means algorithm. If any point moves, the tie rule ensures that the objective strictly decreases. [[centroid#Lemma|this lemma]] has the consequence of fixed assignments causing centre replacement with clusters centroid being unable to increase the SSE.

Each round computes $nk$ distances in $d$ dimensions, at at most $k$ cluster average. The complexity is $O(nkd)$ arithmetic operations. Some special datapoints can have exponential complexity though. 

