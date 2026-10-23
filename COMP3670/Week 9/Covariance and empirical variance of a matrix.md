For real numbers $t_{1},\dots,t_{n}$ with mean $\bar{t}=\frac{1}{n}\sum_{i=1}^n t_{i}$, their empirical variance is defined as $$Var(t_{1},\dots,t_{n})=\frac{1}{n}\sum_{i=1}^n(t_{i}-\bar{t})^2$$
The covariance matrix of a dataset is $$\mathbf{C}=\frac{1}{n}\mathbf{X}_{c}^TX_{c}\in \mathbb{R}^{d \times d}$$With its $(j,\ell)$th entry as $$C_{j,\ell}=\frac{1}{n}\sum_{i=1}^n(x_{ij}-\mu_{j})(x_{i\ell}-\mu_{\ell})$$
The diagonal entry $(j,j)$ is the variance of the feature $j$.
An off diagonal entry averages the products of two features from their respective means. 
using$\frac{1}{n}$ makes variance exactly the average squared deviation.


# Prop 
Every covariance matrix is symmetric, and positive semidefinite (positive operator)