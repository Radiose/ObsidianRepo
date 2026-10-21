# Definition 
let $\mathbf{q}_{1},\dots,\mathbf{q}_{n}$ be an orthonormal eigenbasis of $\mathbf{C}$ (the [[COMP3670/Week 9/covariance|covariance]] matrix) ordered by $\lambda_{1}\geq\dots\geq \lambda_{d}\geq {0}$
For $1 \leq k\leq d$, define $$\mathbf{Q}_k = \begin{pmatrix} | & & | \\ \mathbf{q}_1 & \cdots & \mathbf{q}_k \\ | & & | \end{pmatrix} \in \mathbb{R}^{d\times k}.$$Principle component analysis will retain the $k$ dimensional representation.
Define $$\mathbf{z}_{i}=Q^T_{k}(\mathbf{x}_{i}-\mu)\in \mathbb{R}^k$$Additionally, the corresponding batch of representations is $$\mathbf{Z}=\mathbf{X}_{c}\mathbf{Q}_{k}\in \mathbb{R}^{n \times k}$$Whose $i$th row is $\mathbf{z}_{i}^T$. The retained subspace is $\mathcal{S}_{k}=span \{ \mathbf{q}_{1},\dots,\mathbf{q}_{k} \}$
For a general centred datapoint ($x_{i}-\mu$), $\mathbf{z}_{i}$ gives the coordinates of its projection onto $\mathcal{S}_{k}$.
