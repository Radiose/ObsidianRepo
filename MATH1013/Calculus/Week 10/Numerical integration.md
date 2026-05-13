Numerical [[Definite integral|integration]]
Elementary [[function]]
These are functions that can be obtained from the 5 operations of addition subtraction, multiplication, division and composition. If $f$ is an elementary function, then $f'$ is also elementary, but $\int f(x)dx$ may not be. 
Often, finding an antiderivative of f is not possible algebraically. For example, when we have a function given by measurements from scientific instruments. 
Instead, we attempt to approximate $\int_{a}^b f(x)dx$
We define the error $E$ in our approximation to be the correct value minus the approximation 
Approximation is only helpful when we can bind $|E|$.

## Binding with [[Riemann sum]]s (Midpoint rule)
One method to approximate is the midpoint rule. 
$\sum_{i =0}^{n-1} f(a+i \Delta x)\Delta x \le \int _{a}^bf(x)dx \le \sum_{i=1}^{n}f(a+i \Delta x)\Delta x$ 
left end points                                    right end points 

let $E_{M}=f(x)dx-M_{n}$, where $M_{n}$ is simply the Riemann sum for $f$ over $[a,b]$ using a regular [[partition]] with n intervals and sample points chosen at midpoints
