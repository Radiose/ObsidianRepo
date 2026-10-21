For dimensionality reduction, we want to describe how datapoints differ from each other. As an example, subtracting the same brightness from each image should not create a new direction of variation. 
We therefore subtract the mean datapoint before choosing directions. 

# Mean vector and centred datapoints. 
For $X \in \mathbb{R}^{n \times d}$ with rows $\mathbf{x}^T_{1},\dots,\mathbf{x}^T_{n}$, its mean vector, and centered datapoint is:

$\mu= \frac{1}{n} \sum_{i=1}^n \mathbf{x_{i}}\quad \mathbf{\tilde{x}}_{i}=\mathbf{x}_{i}-\mu$

The centred data matrix is 
$\mathbf{X}_{c}=\mathbf{X}-1{\mu}^T \in \mathbb{R}^{n \times d}$ 

$\mathbf{1}\in \mathbb{R}^n$ has every entry equal to $1$, and $\mu$ is a row, so the product is a matrix. 

Its $i$th row of $\mathbf{X}_{c}$ is $\mathbf{\tilde{x}}_{i}^T$
The mean is just the [[centroid]].

note as well that $\sum_{i=1}^n \mathbf{\tilde{x}}_{i}=\sum_{i=1}^n \mathbf{x}_{i}-n\mu=\mathbf{0}$
Thus each feature column of $X_{c}$ has mean of 0

# Covariance and empirical variance 
For real numbers $t_{1},\dots,t_{n}$ with mean $\bar{t}=\frac{1}{n}\sum_{i=1}^n t_{i}$, their empirical variance is defined as $$Var(t_{1},\dots,t_{n})=\frac{1}{n}\sum_{i=1}^n(t_{i}-\bar{t})^2$$
The covariance matrix of a dataset is $$\mathbf{C}=\frac{1}{n}\mathbf{X}_{c}^TX_{c}\in \mathbb{R}^{d \times d}$$With its $(j,\ell)$th entry as $$C_{j,\ell}=\frac{1}{n}\sum_{i=1}^n(x_{ij}-\mu_{j})(x_{i\ell}-\mu_{\ell})$$
The diagonal entry $(j,j)$ is the variance of the feature $j$.
An off diagonal entry averages the products of two features from their respective means. 
using$\frac{1}{n}$ makes variance exactly the average squared deviation. 


# Importance of the first principle component
Suppose that we can only store one number for each centred datapoint. 
Choosing some unit vector $\mathbf{q}$ lets us store the coordinate $\langle \mathbf{q},\tilde{\mathbf{x}}_{i} \rangle$

### Prop 
For a unit vector $\mathbf{q}\in \mathbb{R}^d$, call $t_{i}=\langle \mathbf{q},\tilde{\mathbf{x}}_{i} \rangle$ 
These coordinates have mean $0$, and their variance is $$Var(t_{1},\dots,t_{n})=\frac{1}{n}\sum(\langle \mathbf{q},\tilde{\mathbf{x}}_{i} \rangle^2 )=\mathbf{q}^T\mathbf{Cq}$$
## ![[principle component scores]]