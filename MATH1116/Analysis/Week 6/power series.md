power [[series]]
# Motivation 
Recall that 
$$\ln(1+x)=\int_{0}^1 \frac{1}{1+t}dt=\int_{0}^x \sum_{n=0} ^\infty(-t)^n dt$$
Because this is an infinite sum, we need [[uniform convergence and L1 norm convergence of sequence of functions|uniform convergence]] to transfer the sum out of the integral. 
Let $x \in[0,1)$ Define $\forall n \in \mathbb{N},\ \forall t\in[0,x]\ \ f_{n}(t):=(-t)^n$
$||f_{n}||_{\infty}=sup_{t\in[0,x]}f_{n}(t):= |-t|^n=x^n$
$\sum_{n=1}^\infty x^n$ converges, thus $\sum_{n=0}^\infty ||f_{n||_{\infty}}$ converges. 
$\implies \sum_{n=0}^\infty f_{n}$ converges uniformly (via [[uniform convergence of a series of sequence of functions#Theorem|this theorem]]). 

Thus, $$\int_{0}^1 \sum_{n=0}^\infty (-t)^ndt=\sum_{n=0}^\infty \int_{0}^1(-t)^ndt=\sum_{n=0}^\infty (-1)^n \frac{x^{n+1}}{n+1}$$
# Definition 
let $(a_{n})_{n \in\mathbb{N}}\in \mathbb{R}^\mathbb{N}$. Let $c \in \mathbb{R}$
Define $f_{n}:\mathbb{R}\to \mathbb{R}$
	$x \mapsto a_{n}(x-c)^n$
The series of functions $\sum_{n=0}^\infty f_{n}$ is called a [[power series]] centred at $0$. 
As an abuse of notation, we write $\sum_{n=0}^\infty a_{n}(x-c)^n$
