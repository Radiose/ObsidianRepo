Dropping hints all the time 
first exam - determinant is subspace? 
second - determinant is linear map?
final - something to do with that 

In final exam, ensure that whenever you solve an integral, state its continuous. 

Check that they really understand the definition in multivariate calculus, then its a simple one dimensional problem. Think about reducing it. 


# Things \#noticed
You can bound the tail of a converging sequence 

the integral test is based off the property that $\sum_{j=n}^m \int_{j-1}^jx_{j} \leq \sum \int_{j-1}^j f(x) = \int_{0}^n f(x)dx$
and that similarly $\int_{j=n}^m \int_{j}^{j+1}x_{j}\geq \sum_{j}^{j+1}f(x)$
This is because $\int_{j}^{j+1} \leq f(j)\leq \int_{j-1}^jf(x)$ ($x_{j}$ is nonincreasing)
Series are discrete analogues of integrals. 

uniform convergence (and L1 norms) seem to be defined on compact sets in the notes. 

COME BACK TO FINAL THEOREM OF SERIES CONVERGENCE


missing limit at $\leq \sum_{k=j}^J ||f_{N_{k+1}}-f_{N_{k}}||$ in uniformly cauchy.



# Importance of uniformity 
Remember that ANY time you want to exchange limits, you NEED uniformity 
The integral is a limit 
The derivative is a limit 
an infinite sum is a limit 

series - rule is you have to think about the sequence of partial sums whenever you come into a problem 
anytime you see a limit - rule is you have to think about uniform convergence 





# Theorem list (analysis)

Cauchy sequence converges 
Proof is: exploit closeness of cauchy to show that upper and lower bound limits of the sequence are equal. This implies that there is a single limit. Then, exploit closeness of sequences upper bound(or lower), and closeness of upper bound to limit and from there, show that the sequence gets close to the limit.


Series:
Most of the background for convergence is based off the idea that the area under the blocks of the sequence goes to zero. 
For example, $\sum_{j=n+1}^{m} \frac{1}{j^2}=\sum_{j=n+1}^m \int_{j-1}^j \frac{1}{j^2}dx \leq \\\sum_{j=n+1}^m \int_{j-1}^j \frac{1}{x^2}dx= \int_{n}^m \frac{1}{x^2}dx=\frac{1}{n}-\frac{1}{m}$ thus cauchy
Similarly 
$\sum_{j=n+1}^m \frac{1}{j}= \sum_{j=n+1}^m \int_{j}^{j+1} \frac{1}{j}dx \geq \sum_{n+1}^m \int_{j}^{j+1}\frac{1}{x}dx = \int_{n+1}^{m+1} \frac{1}{x}dx=\ln(m+1)-\ln(n+1)$ which cannot get small. 

Geometric series: 
$\sum_{n=0}^{\infty}x^n$ converges if $x<1$
Proof: uses the geometric series identity

Sequence goes to zero
Obvious consequence. Can be proven directly by infinite sums and cauchy. 

Comparison test  
Given by bounding the sequence of partial sums (from m to n) above by the larger one, demonstrating cauchy.

Division test:
Proof done by comparison test, making one larger than the other multiplied by the limit.

Integral test 
Uses similar ideas to shown originally 

Ratio test 
Similar idea to regular division test. Uses induction to bound above or below

# Power series 
Motivation is to analyse complication functions as sums of simple ones 

All theorems:
1: Power series either diverge for all x, converge for all, or converge within the open interval $(c-\delta ,c+\delta)$ Note that for 

2: Power series radius of convergence is given by ratio test inverse 
IE $\lim_{ n \to \infty }\frac{a_{n+1}}{a_{n}}=\ell \implies ROC=\frac{1}{\ell}$
Why? Because if $\ell R<1$, it converges, implying that $\frac{1}{\ell}=R$

3:
the integral of a power series is $\int_{c}^x \sum_{n=0}^\infty a_{n}(x-c)^n=\sum_{n=0}^\infty \frac{a_{n}}{n+1}(x-c)^{n+1}$ (by uniformity given by $\delta$ not depending on $x$)
it has the same radius of convergence. 
It has the same radius of convergence because dividing by $n+1$ is only polynomial, it cannot change the exponentials strength. This evident in the proof, when we show that for $\bar{\rho}>\rho>r$, we have that there is some $N$ such that 
$\frac{a_{n}}{n+1}\bar{\rho}^n= \lvert a_{n}\rho^n \rvert \begin{pmatrix} \frac{\bar{\rho}}{p} \end{pmatrix}^n \cdot \frac{1}{n+1} \geq \lvert a_{n}\rho^n \rvert$
for all $n >N$.
This is because $\left( \frac{\bar{\rho}}{\rho} \right)^n$ grows fast and will eventually be larger than $\frac{1}{n+1}$

4:
The derivative of a power series is $\sum_{n=0}^\infty a_{n}(x-c)^n$ is $\sum_{n=0}^\infty (n+1)a_{n+1}(x-c)^{n}$

A similar story, with the $n+1$ not being strong enough to overpower the exponential. Note that the first term $a_{0}$  disappears. 

# Need to revisit: Applications of power series 

# Functions from R^N ->R

Continuity:
Depends on the individual components of the vector  (continuous iff $x_{j}$ is for all j)
Proof: only if was trivial 
if: choose $\delta$ to be $\min_{j \in \{ 1,\dots,n \}} \delta_{j}\left( \frac{\epsilon}{\sqrt{ n }} \right)$ (the smallest $\delta$ such that its $(x_{j}(t+h)-x_{j}(t))< \frac{\epsilon}{\sqrt{ n }}$ )

Differentiability: Same as single variate. 

Arc length parametrisation 
for a $C=\{ x(t): t \in[a,b] \}$, we reparametrize it by 
$y(t)=x(a+t(b-a))$, so its normalised over $[0,1]$
We then define $\sigma(t)=\int_{0}^t \lVert y'(s) \rVert ds$
Think about the idea here. We have that the derivative of a position is velocity, norm is speed, then the integral gives speed summed up over time which is distance. 
We then finally get the inverse, so we give it speed, and obtain time with $\sigma^{-1}(s)=t$
Then, $C=$