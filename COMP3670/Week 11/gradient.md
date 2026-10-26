# Definition
The gradient of $f:\mathbb{R}^m \to \mathbb{R}$ is defined as the vector of its [[multivariate differentiability|partial derivative]]s.
$\nabla f(\mathbf{x})=\left( \frac{\partial f}{\partial x_{1}}(\mathbf{x}),\dots, \frac{\partial f}{\partial x_{m}}(\mathbf{x}) \right)^T$
The sensitivity of $f$ to each of its inputs, collected in some vector. 

We can also utilise [[Linear approximation]]
$\nabla f(\mathbf{x})^T \Delta \mathbf{x}= \frac{\partial f}{\partial x_{1}}\Delta x_{1} +\dots+ \frac{\partial f}{\partial x_{n}}\Delta x_{m}$

# Corollary 
$\nabla f(\mathbf{x})$ is the direction of the steepest ascent, with $\lVert \nabla f(\mathbf{x}) \rVert$ is the slope in that direction.
Meanwhile, $-\nabla f(\mathbf{x})$ is the direction of the steepest descent.

### Proof (informal)
$\nabla f(\mathbf{x})^T \mathbf{u}\leq \lVert \nabla f(\mathbf{x}) \rVert$, via Cauchy schwarz ineq 
We have equality exactly when $\mathbf{u}=\lVert f(\mathbf{x}) \rVert^{-1} \nabla f(\mathbf{x})$
This forces
$$\nabla f^T\mathbf{u} = \frac{\nabla f^T\nabla f}{\|\nabla f\|} = \frac{\|\nabla f\|^2}{\|\nabla f\|} = \|\nabla f\|.$$
This is because $\lVert \mathbf{u} \rVert=1$, so the largest possible is $\lVert \nabla f(\mathbf{x}) \rVert$

# Theorem 
If $f$ has a local minima or maxima at $\mathbf{x}$, and $f$ is [[multivariate differentiability|differentiable]], then $\nabla f(\mathbf{x})=0$.


# Example: [[Gauss least squares]]
The responses are a vector $\mathbf{Y}\in \mathbb{R}^N$, and the data matrix $X\in \mathbb{R}^{N \times m}$ with one row per observation.

$RSS(\theta)=\lVert Y-X\theta \rVert^2=\theta^TX^TX\theta-2\mathbf{Y}^TX\theta+\mathbf{Y}^T\mathbf{Y}$
Thus, the gradient is $$\nabla RSS(\theta)=2X^TX\theta-2X^T\mathbf{Y}=-2X^T(\mathbf{Y}-X\theta)$$

# The Hessian matrix
![[Hessian matrix]]

# Convexity of severable variables 
For multivariate functions, the definition does not change. $f(a \mathbf{x}+b \mathbf{y})\leq af(\mathbf{x})+bf(\mathbf{y})$ for $a,b \geq {0}$ and $a+b=1$

## Theorem 
A well behaved function $f$ is a [[convex function]] if and only its hessian is positive semidefinite (a [[positive operator]]) at every point. 
$\mathbf{u}^T \nabla^2f(\mathbf{x})\mathbf{u} \geq 0$ for every $\mathbf{x}$, and every direction $\mathbf{u}$
If $f$ is convex, and $\nabla f(\mathbf{x})=0$, then $\mathbf{x}$ is a global minimiser. 
This is the same as saying all eigenvalues of the hessian are non negative (link to theorem).

# Relating back to least squares 
The [[Hessian matrix|hessian]] of RSS is $2X^TX$
For any vector $\mathbf{v}$, $\mathbf{v}^T(2X^TX)\mathbf{v}=2(X\mathbf{v})^T(X\mathbf{v})=2 \lVert X \mathbf{v} \rVert \geq 0$
So, its positive and semidefinite, thus convex.
Thus, solving $\nabla RSS(\theta)= \mathbf{0}$ is solving [[Gauss least squares|least squares]].
## Uniqueness of least squares 
Let $\hat{\theta}$ be a critical point.
Thus, $X^T(\mathbf{Y}-X\hat{\theta})=\mathbf{0}$ 
Move it away by some vector $\mathbf{v}$
$$
\begin{aligned}
\mathrm{RSS}(\hat\theta + \mathbf{v}) &= \|(\mathbf{Y} - X\hat\theta) - X\mathbf{v}\|^2 \\
&= \mathrm{RSS}(\hat\theta) - \underbrace{2\mathbf{v}^T X^T (\mathbf{Y} - X\hat\theta)}_{=\,0} + \|X\mathbf{v}\|^2
\end{aligned}
$$
So, moving by $\mathbf{v}$ changes by $X\mathbf{v}$ and costs $\lVert X\mathbf{v} \rVert^2$.
So $\hat{\theta}+\mathbf{v}$ is as good as $\hat{\theta}$ only if $X\mathbf{v}=0$. The predictions do not change at all.

So, if the columns of $X$ are linearly independent, then $X \mathbf{v}=0$ only for one $\mathbf{v}$ (the matrix is [[Injective transformation]] thus $\mathbf{v} \mapsto \mathbf{0}$ is unique)

# Helpful guide 
![[Pasted image 20261026133107.png]]