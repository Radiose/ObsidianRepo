We achieve PCA in these notes via eigen decomposing the covariance matrix. 

# Definition 
let $\mathbf{q}_{1},\dots,\mathbf{q}_{n}$ be an orthonormal eigenbasis of $\mathbf{C}$ (the [[COMP3670/Week 9/covariance|covariance]] matrix) ordered by $\lambda_{1}\geq\dots\geq \lambda_{d}\geq {0}$
For $1 \leq k\leq d$, define $$\mathbf{Q}_k = \begin{pmatrix} | & & | \\ \mathbf{q}_1 & \cdots & \mathbf{q}_k \\ | & & | \end{pmatrix} \in \mathbb{R}^{d\times k}.$$Principle component analysis will retain the $k$ dimensional representation.
Define $$\mathbf{z}_{i}=Q^T_{k}(\mathbf{x}_{i}-\mu)\in \mathbb{R}^k$$Additionally, the corresponding batch of representations is $$\mathbf{Z}=\mathbf{X}_{c}\mathbf{Q}_{k}\in \mathbb{R}^{n \times k}$$Whose $i$th row is $\mathbf{z}_{i}^T$. The retained subspace is $\mathcal{S}_{k}=span \{ \mathbf{q}_{1},\dots,\mathbf{q}_{k} \}$
For a general centred datapoint ($x_{i}-\mu$), $\mathbf{z}_{i}$ gives the coordinates of its projection onto $\mathcal{S}_{k}$.



# Proposition 
for $j=1,\dots,n$, $\mathbf{q}_{j}$ maximises variance among unit vectors orthogonal to $\mathbf{q}_{1},\dots,\mathbf{q}_{j-1}$
The maximum is $\lambda_{j}$. Moreover, the retained scores have mean zero, and covariance $$\frac{1}{n}\mathbf{Z}^T \mathbf{Z}=\mathbf{Q}_{k}^T\mathbf{C}\mathbf{Q}_{k}=diag(\lambda_{1},\dots,\lambda_{k})$$

Thus, a retained coordinate contributes variance $\lambda_{j}$, and the sum of the variances is $\lambda_{1},\dots,\lambda_{k}$
Distinct score coordinates have zero empirical covariance. We say that they are uncorrelated. 


# Reconstruction error

For some matrix $\mathbf{U}\in \mathbb{R}^{d \times k}$ with orthonormal columns, the reconstruction of $\mathbf{x}_{i}$ using the corresponding subspace is $$\hat{\mathbf{x_{i}}}=\mu+\mathbf{U} \mathbf{U}^T(\mathbf{x}_{i}-\mu)$$
Its average squared reconstruction error on the training dataset is $$E(\mathbf{U})= \frac{1}{n}\sum_{i=1}^n \lVert \mathbf{x}_{i}-\hat{\mathbf{x}}_{i} \rVert_{2}^2 $$
# Theorem 
Let $\lambda_{1}\geq\dots\geq \lambda_{d}\geq {0}$ be the eigenvalues of the [[COMP3670/Week 9/covariance|covariance]] matrix $\mathbf{C}$
For each $\mathbf{U}=(\mathbf{u}_{1},\dots,\mathbf{u}_{k})$ with orthonormal columns, $$E(\mathbf{U})=\sum_{\ell=1}^{d}\lambda_{\ell}-\sum_{j=1}^{k} \mathbf{u}^T_{j}\mathbf{Cu}_{j}\geq \sum_{\ell=k+1}^{d} \lambda_{\ell}  $$Equality is attained from $\mathbf{U}=\mathbf{Q}_{k}$. 
Thus, PCA both maximises the sum of retained variance, as well as minimise the average squared construction error among $k$ dimensional subspaces of the data space.

# Corollary 
For any fixed subspace, choosing the dataset mean as the reconstruction offset minimises the average squared error among all offsets. Consequently, PCA gives the best $k$ dimensional affine subspace for the original uncentered data. 

The bound in this corollary also connects the number of samples to the dimension. Whenever $d\geq n$, the centred training datapoints have to lie in a subspace of dimension at most $n-1$, even if the observations consist entirely of noise. 

Exact reconstruction using $n-1$ components is therefore not solely evidence of meaningful low dimensional structure.

The useful question is whether a substantially smaller number of components will retain relevant structure and give a suitable representation of datapoints. 

# Choosing $k$
If $\sum_{j=1}^{d}\lambda_{j}>0$, the explained variance ratio of a $k$ component PCA representation is $$\rho_{k}= \frac{\sum_{j=1}^{k} \lambda_{j}}{\sum_{j=1}^d \lambda_{j}}$$
One way to choose $k$ is to select the smallest $\rho_{k}$ for which $\rho_{k}$ reaches a chosen threshold. 
