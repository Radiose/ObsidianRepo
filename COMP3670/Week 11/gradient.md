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

# The Hessian Matrix 
The hessian of $f$ at $\mathbf{x}$ is the $m \times m$ matrix $\nabla^2f(\mathbf{x})$ of its second [[multivariate differentiability|partial derivative]]s. 
The entry in column $k$ and row $j$ is $$\frac{\partial^2f}{\partial x_{j}\partial x_{k}}$$
For well behaved $f$ it is symmetric. 
