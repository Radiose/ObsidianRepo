---
aliases:
  - converges pointwise
---
Let $f:\mathbb{R}\to \mathbb{R}$ and $f_{n}:\mathbb{R}\to \mathbb{R}$. The [[sequence]] $f_{n}$ converges pointwise if:
$\forall x \in \mathbb{R},\lim_{ n \to \infty }f_{n}(x)=f(x)$

We define a sequence of [[function]]s as the following: $(f_{n})_{n \in \mathbb{N}} \in (\mathbb{R}^\mathbb{R})^\mathbb{N}$



### Examples 
$\forall n \in \mathbb{N},\ \forall x \in \mathbb{R},\ f_{n}(x)=$
				$n^2x \text{  if}$$x \in\left[ 0, \frac{1}{n} \right]$
				 or $0$ otherwise.
Let $f(x):=0 \quad \forall x \in \mathbb{R}$
let $x \in \mathbb{R}$. If $x=0$, then $|f_{n}(x)-f(x)|=0$ $\forall n \in \mathbb{N}$
If $x > 0$, $\exists n \in \mathbb{N}$ such that $x > \frac{1}{n}$. Then, $f_{m}(x)=0\quad \forall m\geq n$
Thus, $\lim_{ n \to \infty }f_{n}(x)=f(x)\forall x \in\mathbb{R}$


# Some important properties of pointwise convergence 
### Property 1: Integral sum 
$\int_{0}^1 f_{}(x) dx=0$
Note that $$\forall n \in \mathbb{N}\ \int_{0}^1 f_{n}(x)dx=\int_{0}^{1/n}n^2xdx$$
Because $f(x)={0}$ unless $x <\frac{1}{n}$
$\implies \int_{0}^{1/n}n^2xdx=n^2\left[ \frac{x^2}{2} \right]_{0}^{1/n} = \frac{1}{2}$

This means $\lim_{ n \to \infty } \int_{0}^1 f_{n}(x)dx = \frac{1}{2} \not=0= \int_{0}^1 \lim_{ n \to \infty }f_{n}(x)dx$
The integral of the limit is not the limit of the integrals. Comparison of pointwise convergence is compatible with finite sums, but not with infinite sums. 

### Property 2: Continuity 
$$
g_n(x) = 
\begin{cases}
0 & \text{if } x = 0, \\
x^n & \text{if } x \in [0,1], \\
1 & \text{if } x \geq 1,
\end{cases}
$$
$\forall n \in \mathbb{N}^*\ x \in \mathbb{R}$ 


Let $g(x) = \mathbb{1}_{[1,\infty)}(x) :=$

$$
g(x) =
\begin{cases}
0 & \text{if } x < 1, \\
1 & \text{if } x \geq 1.
\end{cases}
$$

Let $x =0$. Then, $|g_{n}(x)-g(x)|=0 \quad \forall n \in \mathbb{N}$
If $x \in(0,1)$, then $g_{n}(x)-g(x)$