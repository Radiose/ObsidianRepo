For nonzero vectors $\mathbf{u}\in \mathbb{R}^m$ and $\mathbf{v}\in \mathbb{R}^d$, their **outer product** $\mathbf{uv}^T$ is the $m \times d$ matrix with entry $u_{i}v_{j}$ in position $(i,j)$. It has rank one, with every column a multiple of $\mathbf{u}$, and at least one column nonzero. 
The frobenius norm of $A\in \mathbb{R}^{m \times d}$ is $$\lVert  \mathbf{A} \rVert_{F}= \sqrt{ \sum_{i=j}^n\sum_{j=1}^d a_{ij}^2}$$
Thus, $\lVert A -{B} \rVert_{F}^2$ is the sum of squared entry wise errors. It is also the sum of the squared [[Euclidian norm]]s of the rows of $A -{B}$
