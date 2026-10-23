For $X \in \mathbb{R}^{n \times d}$ with rows $\mathbf{x}^T_{1},\dots,\mathbf{x}^T_{n}$, its mean vector, and centered datapoint is:

$\mu= \frac{1}{n} \sum_{i=1}^n \mathbf{x_{i}}\quad \mathbf{\tilde{x}}_{i}=\mathbf{x}_{i}-\mu$

The centred data matrix is 
$\mathbf{X}_{c}=\mathbf{X}-1{\mu}^T \in \mathbb{R}^{n \times d}$ 

$\mathbf{1}\in \mathbb{R}^n$ has every entry equal to $1$, and $\mu$ is a row, so the product is a matrix. 

Its $i$th row of $\mathbf{X}_{c}$ is $\mathbf{\tilde{x}}_{i}^T$
The mean is just the [[centroid]].

note as well that $\sum_{i=1}^n \mathbf{\tilde{x}}_{i}=\sum_{i=1}^n \mathbf{x}_{i}-n\mu=\mathbf{0}$
Thus each feature column of $X_{c}$ has mean of 0