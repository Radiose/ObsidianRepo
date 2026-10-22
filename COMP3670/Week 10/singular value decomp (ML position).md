SVD is a method to 

Every nonzero matrix $\mathbf{A}\in \mathbb{R}^{m \times d}$ of rank $r$ admits a factorisation $$\mathbf{A}=\mathbf{U}_{r}\sum_{r}\mathbf{V}_{r}^T$$
Where $\mathbf{U}_{r}\in \mathbb{R}^{m \times r},\quad \sum_{r}\in \mathbb{R}^{r \times r},\quad \mathbf{V}_{r}\in \mathbb{R}^{d \times r}$

Where $\mathbf{U}_{r}= \begin{pmatrix} | & & | \\ \mathbf{u}_1 & \cdots & \mathbf{u}_k \\ | & & | \end{pmatrix}\quad \mathbf{V}_{r}=\begin{pmatrix} | & & | \\ \mathbf{v}_1 & \cdots & \mathbf{v}_k \\ | & & | \end{pmatrix}$ , 
$\sum_{r}=diag( \sigma_{1},\dots,\sigma_{r})= \begin{bmatrix}\sigma_{1}  & . & . & . & 0 \\  .  & \sigma_{2} & . &  & 0 \\ .  &  & . &  &  \\ .  &  &  & . &   \\   &  &  &  & \sigma_{r}\end{bmatrix}$
The columns of $\mathbf{U}_{r},\quad \mathbf{V}_{r}$ are orthonormal, and $\sigma_{1}\geq \dots \geq \sigma_{r} \geq 0$
These numbers are the singular values.
$\mathbf{u}_{i},\mathbf{v}_{i}$ are the corresponding left and right singular vectors. 

We call this the compact/truncated form of the matrix form of [[singular value decomposition]].

# Proposition 1
For each singular-vector pair
$A \mathbf{v}_{i}= \sigma_i\mathbf{u}_{i}$
$A^T \mathbf{u}_{i}= \sigma_{i}\mathbf{v}_{i}$
Their eigenvector equations are $A^TA_{i}= \sigma^2\mathbf{v}_{i}$ and $AA^T \mathbf{u_{i}}= \sigma^2_{i}\mathbf{u}_{i}$ (from combining both)
Both matrices have positive eigenvalues $\sigma_{1}^2,\dots,\sigma_{r}^2$ counted with multiplicity. 
Their remaining eigenvalues are zero. there is $d-r$ for $A^TA$ and $m-r$ for $AA^T$ via RNT

For any input $\mathbf{x}$, $\mathbf{Ax}= \mathbf{U}_{r} \sum_{r} \mathbf{V}_{r}^T \mathbf{x}$, has three stages. 
Extract coordinates along the $\mathbf{v}_{i}$, scale them by $\sigma$ and combine outputs $\mathbf{u}_{i}$.
Since both singular vectors have unit length(norm of 1),  $\sigma_{i}$ measures how much $\mathbf{A}$ stretches the particular input direction $\mathbf{v}_{i}$


# Using truncation to get the best low rank approximation 
The expansion $\sum_{i}\sigma_{i}\mathbf{u}_{i}\mathbf{v}_{i}^T$ separates a matrix into simple contributions. If only a few contributions are large, we may be able to keep a small number, while changing the entries only slightly. 

![[Frobenius norm]]