SVD is a method to 

Every nonzero matrix $\mathbf{A}\in \mathbb{R}^{m \times d}$ of rank $r$ admits a factorisation $$\mathbf{A}=\mathbf{U}_{r}\sum_{r}\mathbf{V}_{r}^T$$
Where $\mathbf{U}_{r}\in \mathbb{R}^{m \times r},\quad \sum_{r}\in \mathbb{R}^{r \times r},\quad \mathbf{V}_{r}\in \mathbb{R}^{d \times r}$

Where $\mathbf{U}_{r}= \begin{pmatrix} | & & | \\ \mathbf{u}_1 & \cdots & \mathbf{u}_k \\ | & & | \end{pmatrix}\quad \mathbf{V}_{r}=\begin{pmatrix} | & & | \\ \mathbf{v}_1 & \cdots & \mathbf{v}_k \\ | & & | \end{pmatrix}$ , 
$\sum_{r}=diag( \sigma_{1},\dots,\sigma_{r})= \begin{bmatrix}\sigma_{1}  & . & . & . & 0 \\  .  & \sigma_{2} & . &  & 0 \\ .  &  & . &  &  \\ .  &  &  & . &   \\   &  &  &  & \sigma_{r}\end{bmatrix}$
The columns of $\mathbf{U}_{r},\quad \mathbf{V}_{r}$ are orthonormal, and $\sigma_{1}\geq \dots \geq \sigma_{r} \geq 0$
These numbers are the singular values.
$\mathbf{u}_{i},\mathbf{v}_{i}$ are the corresponding left and right singular vectors. 

We call this the compact/truncated form of the matrix form of [[singular value decomposition]].

We can connect the eigenvalues of $A^TA$ because $A$ is a real operator, so its adjoint is its transpose, so then there is a theorem that states that it $TT^*$ is a positive operator, and we can define singular values of $A^TA$
# Proposition 1
For each singular-vector pair
$A \mathbf{v}_{i}= \sigma_i\mathbf{u}_{i}$
$A^T \mathbf{u}_{i}= \sigma_{i}\mathbf{v}_{i}$
Their eigenvector equations are $A^TA_{i}= \sigma^2\mathbf{v}_{i}$ and $AA^T \mathbf{u_{i}}= \sigma^2_{i}\mathbf{u}_{i}$ (from combining both)
Both matrices have positive eigenvalues $\sigma_{1}^2,\dots,\sigma_{r}^2$ counted with multiplicity. This is because we treat $A^TA$ as a positive 
Their remaining eigenvalues are zero. there is $d-r$ for $A^TA$ and $m-r$ for $AA^T$ via RNT

For any input $\mathbf{x}$, $\mathbf{Ax}= \mathbf{U}_{r} \sum_{r} \mathbf{V}_{r}^T \mathbf{x}$, has three stages. 
Extract coordinates along the $\mathbf{v}_{i}$, scale them by $\sigma$ and combine outputs $\mathbf{u}_{i}$.
Since both singular vectors have unit length(norm of 1),  $\sigma_{i}$ measures how much $\mathbf{A}$ stretches the particular input direction $\mathbf{v}_{i}$


# Using truncation to get the best low rank approximation 
The expansion $\sum_{i}\sigma_{i}\mathbf{u}_{i}\mathbf{v}_{i}^T$ separates a matrix into simple contributions. If only a few contributions are large, we may be able to keep a small number, while changing the entries only slightly. 
We seek to get a precise definition of "large" and "simple".
We can view Axler c7F, where its shown that some k is the best rank k approximation of some matrix. 

![[Frobenius norm]]

## Rank K truncated SVD 
For a matrix with compact SVD $\mathbf{A}=\sum_{i=1}^k \sigma_{i}\mathbf{u}_{i}\mathbf{v}_{i}^T$ and $1 \leq k \leq r$, its rank $k$ truncated [[singular value decomposition]] is $$A_{k}=\sum_{i=1}^k \sigma_{i}\mathbf{u}_{i}\mathbf{v}_{i}^T= \mathbf{U}_{k}\sum_{k}\mathbf{V}_{k}^T$$
Where the subscript $k$ retains the first $k$ columns of each vector matrix, and the first $k$ diagonal entries of $\sum_{r}$. What we are doing here is just removing the columns that arent

Every column of $\mathbf{A}_{k}$ is a combination of $\mathbf{u}_{1},\dots,\mathbf{u}_{k}$.
Conversely, $\mathbf{A}_{k} \mathbf{v}_{i}=\sigma_{i}\mathbf{u}_{i}$ for $i < k$.
Each of these $k$ independent vectors lies in $col(\mathbf{U}_{k})$

## Eckhart young theorem
For every matrix $\mathbf{B} \in \mathbb{R}^{m \times d}$, with rank at most $k$.
$$\lVert \mathbf{A}-\mathbf{B} \rVert_{F}^2 \geq \lVert \mathbf{A}-\mathbf{A}_{k} \rVert_{F}^2  = \sum_{i = k+1}^r \sigma^2_{{i}}$$
In particular $\mathbf{A}_{k}$ is the best approximation among all matrices of rank at most k. 


The truncated singular value decomp gives a best rank-at-most-$k$ approximation. 
The error is the sum of the square of the **discarded** singular values. 
When $k=r$, the reconstruction is exact, so $A_{k}$ is a is a best approximation among all matrices of rank at most $r$.

Storing the three truncated factors takes $k(m+d+1)$ numbers instead of $md$. Because MD is the number of entries in some $M \times D$ matrix. 
There is a saving in storage only when $k$ is sufficiently small. 

Mathematical optimality only relates to squared reconstruction error, rather than success on an ML task. 

# Missing entries

Suppose we wanted to predict how much some user will like a movie(based off a numerical rating system).
BUT, in this case, we are missing entries, (user hasnt rated every type of movie)
The goal here is to minimise our loss on observed entries, via alternating least squares.
This is because ordinary SVD requires a numerical value in each position and additionally, it would not be mathematically accurate to state a lack of a rating is zero, as that would indicate an actual rating of zero.

### What we will use
A user item rating matrix $\mathbf{R}\in \mathbb{R}^{m \times n}$ records the ratings of $n$ users for $m$ items. 
A latent factor model assigns a vector $\mathbf{p}_{i} \in \mathbb{R}^k$ to a user $i$, and a vector $\mathbf{q}_{j}\in \mathbb{R}^k$
We aim to predict $\hat{r_{i,j}}=\langle \mathbf{p_{i},q_{j}} \rangle$
Stacking users into rows of $\mathbf{P}\in \mathbb{R}^{n \times k}$ and item vectors into rows of $\mathbf{Q}\in \mathbb{R}^{m \times k}$
gives $\hat{\mathbf{R}}=\mathbf{PQ}^T$

## Regularised K factor model 
Let $\Omega \subset \{ 1,\dots,n \}\times \{ 1,\dots,m \}$ be the set of observed training points. 
A regularised $k$ factor model, fits the user and item vectors by minimising $$L(\mathbf{P,Q})= \sum_{(i,j)\in \Omega }(r_{i,j}-\langle \mathbf{p_{i}}-\mathbf{q}_{j} \rangle )^2 +\lambda \left( \sum_{i=1}^n \lVert \mathbf{p}_{i} \rVert_{2}^2+ \sum_{j=1}^m \lVert \mathbf{q}_{j} \rVert_{2}^2   \right), \quad \lambda \geq {0}$$The squared norm term is a regularisation penalty (on the left controlled by $\lambda$). As in [[Support vector machine]]s, fitting the data competes with keeping parameters small.
Our factor count $k$, and penalty strength $\lambda$ are hyperparameters, which are selected using validation ratings.
The learnt $\mathbf{P},\mathbf{Q}$ don't need to orthonormal columns either.

If all entries are observed, $\lambda=0$ means that truncated SVD provides a global minimiser of this objective for $k \leq rank(R)$
However, with missing entries, or a positive $\lambda$, the conclusion no longer follows from the Eckhart young theorem.
How to learn the factors?
Fix item vectors temporarily, then each predicted rating is a linear function of the user vector, so fitting that user is a squared error linear model problem.
With a positive penalty, it also charges for the size of the user vector.
We then alternate between the roles of users and items. This gives alternating least squares. 