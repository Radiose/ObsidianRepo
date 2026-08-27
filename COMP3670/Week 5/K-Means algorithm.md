Input $\mathcal{D}=\{ \mathbf{x_{1}},\dots,\mathbf{x_{n}} \}\subset \mathbb{R}^d$ and a [[partition]] into $k \geq {2}$ nonempty clusters. 

We compute the [[centroid]] $\mathbf{c}_{r}$ of each cluster $\mathcal{C}_{r}$
We then assign each $\mathbf{x_{i}}$ to a [[clustering|cluster]] whos [[centroid]] is closest.
If tied, we retain the current cluster. 
Then, we repeat until no cluster changes. 

