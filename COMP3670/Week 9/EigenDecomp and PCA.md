# Building to it

For dimensionality reduction, we want to describe how datapoints differ from each other. As an example, subtracting the same brightness from each image should not create a new direction of variation. 
We therefore subtract the mean datapoint before choosing directions. 




# Spectral theorem 
For every real, symmetric matrix, $A \in \mathbb{R}^{d \times d}$ has some orthonormal basis with real eigenvalues. 
This is just the [[real spectral theorem]], which comes from $A$ being symmetric, implying that $A$ is also self adjoint.





# Positive, semidefinite matrix 
A symmetric matrix $A$, and the scalar $\mathbf{v}^T\mathbf{Av}$ is its quadratic form evaluated at $\mathbf{v}$. The matrix is positive semidefinite if $\mathbf{v}^T\mathbf{Av} \geq 0 \quad \forall \mathbf{v}\in \mathbb{R}^d$
This is also called a [[positive operator]].
Note that via LINK TO THEOREM, all [[eigenvalue]]s of $A$ are nonnegative. 




![[Mean vector and centred datapoints.]]


![[Covariance and empirical variance of a matrix]]




# Last steps


Suppose that we can only store one number for each centred datapoint. 
Choosing some unit vector $\mathbf{q}$ lets us store the coordinate $\langle \mathbf{q},\tilde{\mathbf{x}}_{i} \rangle$

### Prop 
For a unit vector $\mathbf{q}\in \mathbb{R}^d$, call $t_{i}=\langle \mathbf{q},\tilde{\mathbf{x}}_{i} \rangle$ 
These coordinates have mean $0$, and their variance is $$Var(t_{1},\dots,t_{n})=\frac{1}{n}\sum(\langle \mathbf{q},\tilde{\mathbf{x}}_{i} \rangle^2 )=\mathbf{q}^T\mathbf{Cq}$$



## Principle component scores
 ![[principle component scores]]

# Theorem 
Let $\mathbf{C}$ have an [[orthonormal vectors|orthonormal basis]] of eigenvectors, ordered so that $\lambda_{1}\geq \lambda_{2} \geq\dots \geq \lambda_{n}\geq {0}$
Then $$\max_{\lVert \mathbf{q} \rVert_{2}=1 }\mathbf{q}^T \mathbf{Cq}=\lambda_{1}$$
So each unit vector in the eigenspace of $\lambda_{1}$ maximise the the same things that principle components do. So, $\mathbf{q}_{1}$ must be a first principle component. 

# PCA 
![[Principle component analysis]]