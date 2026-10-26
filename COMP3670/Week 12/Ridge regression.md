This is a form of [[parametric regression|linear regression]] similar to [[Gauss least squares]].
Its motivation is given by high order polynomials overfitting training data.
One option is to keep the polynomials in high order, but stop coefficients becoming large.

# Definition 
$$\hat{\theta}^{ridge}= arg \min_{\theta}\lVert \mathbf{Y}-X\theta \rVert^2 + \lambda \lVert \theta \rVert^2 \text{ for }\lambda > 0$$				                                                           fit              penalty
$$\theta^{RIDGE}=(X^TX+\lambda I)^{-1}X^T \mathbf{Y}$$Comparing this to [[Soft margin SVM]], *hinge* $+ \lVert \mathbf{w} \rVert^2$ there, *squared* $+\ \ \lambda \lVert \theta \rVert^2$ here
$\lambda$=0 is used in regular least squares. Large $\lambda$ forces the coefficients to $0$.

## Derivation 
The criterion is $J(\theta)=\lVert \mathbf{Y}-X\theta \rVert^2+ \lambda \lVert \theta \rVert^2$
The table of [[gradient]]s give $\nabla J(\theta)=-2X^T(\mathbf{Y}-X\theta)+2\lambda \theta$
Setting to zero yields $(X^TX+\lambda I)\theta =X^T\mathbf{Y}$ with [[Hessian matrix|Hessian]] $2(X^TX+\lambda I)$
Adding $\lambda I$ increases every [[eigenvalue]] of $X^TX$ by $\lambda$, so they are at least $\lambda >0$
### Penalty and convexity 
With $\lambda >0$, the ridge criterion is **strictly convex**. The minimiser exists, and is unique. $X^TX+\lambda I$ is always invertible, **even** when $X$ does not have full rank. 
$\lambda$ tunes complexity continuously, rather than regular polynomial regression. 
$\hat{h}$ is the best fit in the **chosen basis** subject to some fit on the polynomials.

