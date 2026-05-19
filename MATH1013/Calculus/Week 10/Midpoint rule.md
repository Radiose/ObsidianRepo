## Midpoint rule
One method to approximate is the midpoint rule. 
$\sum_{i =0}^{n-1} f(a+i \Delta x)\Delta x \le \int _{a}^bf(x)dx \le \sum_{i=1}^{n}f(a+i \Delta x)\Delta x$ 
left end points                                    right end points 

let $E_{M}=f(x)dx-M_{n}$, where $M_{n}$ is simply the [[Riemann sum]] for $f$ over $[a,b]$ using a regular [[partition]] with n intervals and sample points chosen at midpoints. 

### Binding the error 
[[theorem]]:
If $K$ is a real number such that $|f''(x)| \le K \forall x \in [a,b]$, then 
$|E_{m}|=\frac{K(b-a)^3}{24n^2}$

Provided we can bind f''(x) in the closed interval \[a,b], we know how to choose n so that we can be sure that the error is less than or equal to some certain demand we have. Remember that a and b is the interval we approximate over (top and bottom of integral)
### Putting it together 
Example: approximate $\int_{0}^1e^{x^2}dx$ within 0.01 of the correct answer 
$f''(x)=(2+4x^2)e^{x^2}$
Now, we need to find K such that f''(x) is always less than it in the interval. Because these two [[function]]s are always increasing, there is no need to do [[The closed interval method]]. However, if they werent, you would do the CIM using the derivative of f''(x), which is the third [[Derivative]] of x. 
thus, the largest y in \[0,1] is 1. 
$f''(x) \le f''(1) = 6e$ 

Now we use the binding theorem 
$|E_{m}|=\frac{K(b-a)^3}{24n^2}<0.01$
solving algebraically
$n> \sqrt{ \frac{e}{0.004} } \approx {8}.24$
Thus we now solve the [[Riemann sum]] using 9 partitions, taking the midpoint of each [[partition]]