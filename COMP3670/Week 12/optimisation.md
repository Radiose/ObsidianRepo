# Definition 
Given some **objective function** $J:\mathbb{R}^m \to \mathbb{R}$, an optimisation problem asks $$\mathbf{\hat{\theta}}\in arg \min_{\mathbf{\theta} \in \mathbb{R}}J(\theta)$$
We call such a $\mathbf{\hat{\theta}}$ an optimiser, with $J(\mathbf{\hat{\theta}}$ as a minimiser.
Relating back to the [[supervised learning framework]], $J$ is the sample error, and $\theta$ are the parameters of the model.

In a **constrained optimisation problem**, $\theta$ must also satisfy other conditions.

![[Pasted image 20261026160221.png]]

# Minimising the [[gradient]]
There are two main ways to minimise the gradient,
1: Using a formula, such as seen in [[gradient#Relating back to least squares|this note]].
2: Via iteration 
# Functions that preserve [[convex function|convexity]]
These are
1: Sums and positive multiples of convex functions 
2: A convex function of a [[linear map]] such as $\theta \mapsto X\theta - \mathbf{Y}$ 
3: The maximums of convex functions.

Some examples 
![[Pasted image 20261026160547.png]]

## Importance of convexity 
There are some key properties that make convex functions ultra important to gradient optimisation 
- Every [[Critical point of a function|critical point]] is a **global** minima. 
- Every local minima is global 
- The starting point does not matter for the end point 

### Strictly\merely convex 
This is when there is a unique minima, and merely convex means that there could be many local minima, each as good as each other.

# [[Gauss least squares|least squares]] in [[matrix]] form 

Recall [[parametric regression|linear regression]]s formula, $Y= \theta_{0}\phi_{0}(\mathbf{X})+\dots+\theta_{k}\phi_{k}(\mathbf{X}) + \epsilon$
We stack these into vectors, giving $Y=\begin{bmatrix}y_{1}  \\  . \\  . \\  . \\  y_{k}\end{bmatrix}$ and $X=\begin{bmatrix}\phi_{0}(\mathbf{X}_{1}) & . & . & . & \phi_{k}(\mathbf{X}_{1})  \\ .  \\ .   \\ .   \\  \phi_{0}(\mathbf{X_{n}}) & . & . & . &\phi_{k}(\mathbf{X_{n}}) \end{bmatrix}$
With $RSS(\theta)=\lVert \mathbf{Y}-X\theta \rVert^2$
Note that $\mathbf{X}_{1}$ denotes the first entry in $\mathbf{X}$

### WRT the gradient 
Recall that $\nabla RSS(\theta)=-2X^T(\mathbf{Y}-X\theta)$
Set it to 0.
$$
-2X^T(\mathbf{Y} - X\boldsymbol\theta) = 0 \implies 2X^T\mathbf{Y} = 2X^TX\boldsymbol\theta \implies X^TX\boldsymbol\theta = X^T\mathbf{Y}
$$
A linear system of $m$ equations in $m$ unknowns gives us that if $X$ has full rank, then $X^TX$ is invertible and thus uniquely solvable.

Because the model is **linear** in $\theta$, the normal equations can be solved in closed form. 
If $X$ has full rank, then $$X^TX\theta=X^T\mathbf{Y} \implies \hat{\theta}=(X^TX)^{-1}X^T\mathbf{Y}$$With $\hat{h}(\mathbf{x})=\Phi(\mathbf{x})^T\hat{\theta}$
Where, $\Phi(\mathbf{x})$ is $\mathbf{x}$ applied to all basis vectors.

# ridge regression 
![[Ridge regression]]

![[gradient descent]]


![[non linear SVM]]