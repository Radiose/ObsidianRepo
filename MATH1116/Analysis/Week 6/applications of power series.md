There are three main applications of [[power series]] discussed in MATH1116. 

# Complex functions 
We can use power series to define functions $f: \mathbb{C} \to \mathbb{C}$.
For example, $e^z:=\sum_{n=0}^\infty \frac{z^n}{n!}\quad \forall z \in \mathbb{C}$

# Numerical analysis 

Using the definition of $e^z$ from before, if we want to approximate $e^z$, we can use the definitions from the power series to define them numerically. 

For example, $\left\lvert  e^x - \sum_{n=0}^N \frac{x^n}{n!}  \right\rvert$ is the difference between the actual $e^x$ and the approximation we have from $0$ to $N$. 

So for $x \in \left( 2,2 \right)$ to get $|e^x -\sum_{n=0}^N \frac{x^n}{n!}|\leq 10^{-4}$, we know our $x$ is never going to be greater than 2. 
Thus, we aim to bind it. 
$|e^x-\sum_{n=0}^N \frac{x^n}{n!}|=\sum_{N+1}^\infty \frac{2^n}{n!}=9 \sum_{N+1}^\infty\left( \frac{2}{3} \right)^n =18 \times \frac{\frac{2}{3}^{N+1}}{1-\frac{2}{3}}$ 

# Differential equations 

Power series can be used to solve [[ordinary differential equation|ODE]]s. Take the example of $y'(x)=-xy(x)\quad\forall x \in \mathbb{R},\quad y(0)=1$

Assume that $y(x)=\sum_{n=0}^\infty a_{{n}}x^n\quad\forall x \in \mathbb{R}$ 
Then, $\sum_{n=0}^\infty(n+1)a_{n+1}x^n =-x \sum_{n=0}^\infty a_{n}x^n=-\sum_{n=0}^\infty a_{n}x^{n+1}=\sum _{n=1}^\infty a_{n-1}x^n$
$\implies y(0)=a_{0}=1$

Similarly, $y'(0)=0$
$\implies \sum_{n=0}(n+1)a_{n+1}0^n=0$
$\implies a_{1}=0$
