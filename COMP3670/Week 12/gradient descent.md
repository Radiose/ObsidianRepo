# Motivation
Recall [[logistic regression]].
We denote $\eta(\mathbf{x|\theta})$ as $\sigma(z)$

The probability of class 1 is $\sigma(\mathbf{w}^T\mathbf{x})$ with a $1$ in front of the features so that the bias is in one of the weights. 
The objective is $J(\mathbf{w})= \frac{1}{N} \sum_{i}\ell_{i}(\mathbf{w})$ where $\ell_{i}(\mathbf{w})=-Y_{i}\log \sigma(\mathbf{w}^T\mathbf{X}_{i})-(1-Y_{i})\log(1-\sigma(\mathbf{w}^T\mathbf{X}_{i}))$

The gradient of cross entropy loss is 
$$\nabla \ell_{i}(\mathbf{w})=(\sigma(\mathbf{w}^T\mathbf{X}_{i})-Y_{i})\mathbf{X}_{i}\quad \text{and}\quad \nabla J(\mathbf{w})=\frac{1}{N}\sum_{i=1}^N(\sigma(\mathbf{w}^T\mathbf{X}_{i})-Y_{i})\mathbf{X}_{i}$$
where $\ell_{i}$ is the loss on a singular observation.

However, there is **no** formula to solve this that we currently know. This is because $\mathbf{w}$ is in $\sigma(\mathbf{w})$ which is not linear, so no linear algebra can solve for the optimal solution.

# The algorithm 

1: Choose a starting point, $\mathbf{\theta}(0)$
2: For each iteration $t=0,1\dots$ compute the gradient at the current point and update  $$\mathbf{\theta}(t+1)=\mathbf{\theta}(t)-\alpha \nabla J(\mathbf{\theta}(t))$$
3: Repeat 2 until a stopping rule is met.

$\alpha >0$ is the **learning rate**, how far we move in the downward direction.
It is a hyperparameter, set manually and not learnt from data.

## The learning rate 
The learning rate of gradient descent is dependent on the magnitude of the second derivative of $J$.
The greater it is, the smaller the learning rate must be. 
![[Pasted image 20261026183500.png]]

# The theoretical guarantees of gradient descent (gradient descent on a convex object)
Let $J$ be [[convex function|convex]], and well behaved with curvature $(J'')$ at most $K$ in any direction and at every point (no eigenvalue of the [[Hessian matrix|Hessian]] exceeds $K$)
If the learning rate satisfies $\alpha \leq \frac{1}{K}$, then from any starting point $\mathbf{\theta}(0)$, we have that $$J(\theta(t))-J(\hat{\theta})= \frac{\lVert \mathbf{\theta}_{0}- \hat{\mathbf{\theta}} \rVert^2}{2 \alpha t} $$
This means that after $t$ steps, the objective is within a constant $t$ of its minimum. 
Ten times more steps, the bound is 10 times smaller.

## Stopping rules 
We must decide where to stop, there are usually 4 rough rules 
- The gradient is small $\implies$ we are almost at a critical point 
- The objective has stalled $\implies$ no decrease for a while 
- The validation error has stopped improving
- Exceeds budget (we have a fixed number of iterations)

# Gradient descent for [[Gauss least squares|least squares]], [[Ridge regression]], [[logistic regression]]
![[Pasted image 20261026184133.png]]


# Stochastic gradient descent
![[Stochastic gradient descent]]