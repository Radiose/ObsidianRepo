Series, like [[sequence]]s can [[Convergence of a sequence|converge]]. 
Let $(x_{j})_{j \in \mathbb{N}}\in \mathbb{R}^{\mathbb{N}}$. We define $s_{n}=\sum_{j=0}^n x_{j}$. If $(s_{n})_{n \in \mathbb{N}}$ converges, we denote its limit by $\sum_{j=0}^\infty x_{j}$.

Some AON 
If $(s_n)_{n\in\mathbb{N}}$ converges, we say that the series $\sum_{j=0}^\infty x_j$ converges.
If $(s_n)_{n\in\mathbb{N}}$ diverges, we say that the series $\sum_{j=0}^\infty x_j$ diverges.




Series can be thought of as the discrete form analogous to the [[Definite integral|integral]]. The following remark helps relate them easier. 
### Remark
$\int_{0}^{n+1}f(x)dx=\sum_{j=0}^n \int_{j}^{j+1}x_{j}dx +\sum_{j=n+1}^\infty \int_{j}^{j+1} x_{j}dx$

If $\sum_{j=0}^\infty$ converges, 

$\sum_{j=0}^\infty x_{j}=\int_{0}^\infty f(x)dx:=\lim_{ M \to +\infty }\int_{0}^Mf(x)dx$

The sequence of partial sums converges. That is the most important fact. 


# Geometric series 

We show that $\sum_{n=0}^\infty x^n$ converges if and only if $x<1$

To see this

$$
(1-x)\sum_{j=0}^{n} x^j = \sum_{j=0}^{n} x^j - \sum_{j=0}^{n} x^{j+1} = \sum_{j=0}^{n} x^j - \sum_{j=1}^{n+1} x^j = 1 - x^{n+1}.
$$

Therefore

$$
\forall x \neq 1, \forall n \in \mathbb{N}, \quad \sum_{j=1}^{n} x^j = \frac{1-x^{n+1}}{1-x}.
$$

If $x < 1$, then $\displaystyle\sum_{j=0}^{n} x^j \xrightarrow[n \to +\infty]{} \frac{1}{1-x}$.

If $x > 1$, then $\displaystyle\sum_{j=0}^{n} x^j = \frac{x^{n+1}-1}{x-1} \xrightarrow[n \to +\infty]{} +\infty$.

If $x = 1$, then $\displaystyle\sum_{j=0}^{n} x^j = n+1 \xrightarrow[n \to +\infty]{} +\infty$.




# Example 

We can use the definition of a Cauchy sequence to show us some series converges. 
Let $m, n \in \mathbb{N}$ and $m \geq n$.

Then
Note that this is because $\frac{1}{j^2}$ is monotonously decreasing. Thus, $\forall j \in \mathbb{N}$, $\int_{j-1}^j\frac{1}{j^2}dx \leq \int_{j-1}^j \frac{1}{x^2}dx$. This is because we are taking the right end point here. Similarly, $\sum_{j=m}^{n-1}\int_{j}^{j+1} \frac{1}{x^2}dx\leq \sum_{j=m}^{n-1}\int_{j}^{j+1} \frac{1}{j^2}dx$.
The actual proof:


$$
\sum_{j=n+1}^{m} \frac{1}{j^2} = \sum_{j=n+1}^{m} \int_{j-1}^{j} \frac{1}{j^2} \, dx \leq \sum_{j=n+1}^{m} \int_{j-1}^{j} \frac{1}{x^2} \, dx = \int_{n}^{m} \frac{1}{x^2} \, dx = \frac{1}{n} - \frac{1}{m}.
$$

Let $\varepsilon > 0$. Pick $N \in \mathbb{N}$ such that $\frac{1}{N} \leq \frac{\varepsilon}{2}$. Then $\forall n, m \geq N$,
We use the [[Cauchy sequence]] definition to aid us. 

$$
\left| \sum_{j=0}^{m} \frac{1}{j^2} - \sum_{j=0}^{n} \frac{1}{j^2} \right| = \left| \sum_{j=n+1}^{m} \frac{1}{j^2} \right| \leq \frac{1}{n} + \frac{1}{m} \leq \varepsilon.
$$

Therefore $\left( \sum_{j=1}^{n} \frac{1}{j^2} \right)_{n \in \mathbb{N}}$ is Cauchy, and therefore converging. Or, the **sequence of partial sums** defined by the series is Cauchy.  







# More theorems for convergence of series 

## Theorem 1 (elements tend to 0)
If $\sum_{j=0}^\infty x_{j}$ converges, then $x_{j}\xrightarrow[j \to \infty]{}0$
### Proof
Let $\sum_{j=0}^\infty x_{j}=l$
This implies $x_{n}=\sum_{j=0}^n x_{j}-\sum_{j=0}^{n-1}x_{j} \to l-l=0$

IMPORTANT: the converse of this does not apply.  (simple example is $\frac{1}{n}$)
Proof of the divergence of $\sum_{n=1}^\infty \frac{1}{n}$:
using the integral trick shown above 
$\sum_{n=1}^N \frac{1}{n}=\sum_{n=1}^N \int_{n}^{n+1} \frac{1}{n}dx \geq \sum_{n=1}^N \int_{1}^{n+1} \frac{1}{x}dx=\ln(n+1) \xrightarrow[n \to \infty]{}\infty$
We start to understand that a series must not just approach zero, but it must also approach it fast enough. 


## Theorem 2 (converging series bounds smaller one)
Let $(x_j)_{j\in\mathbb{N}}, (y_j)_{j\in\mathbb{N}} \in \mathbb{R}^{\mathbb{N}}$ be such that $0 \leq x_j \leq y_j, \forall j \in \mathbb{N}$.
Then $\sum_{j=0}^{\infty} y_j$ converges implies $\sum_{j=0}^{\infty} x_j$ converges.

*Proof.* Let $\varepsilon > 0$. Pick $N \in \mathbb{N}$ such that $\forall n \geq m \geq N$,

$$\left|\sum_{j=m}^{n} y_j\right| < \varepsilon.$$

Then $\forall n \geq m \geq N$,

$$\left|\sum_{j=m}^{n} x_j\right| = \sum_{j=m}^{n} x_j \leq \sum_{j=m}^{n} y_j < \varepsilon.$$

Therefore $\sum_{j=0}^{\infty} x_j$ converges. $\blacksquare$
## Theorem 3 (division of series converging implies convergence)

Let $(x_j)_{j\in\mathbb{N}}, (y_j)_{j\in\mathbb{N}} \in (0,\infty)^{\mathbb{N}}$.
If $\lim_{j\to+\infty} \dfrac{x_j}{y_j} = \ell \in (0,\infty)$, then $\sum_{j=0}^{\infty} x_j$ converges $\iff \sum_{j=0}^{\infty} y_j$ converges.

*Proof.* Since $\dfrac{x_j}{y_j} \xrightarrow[j\to+\infty]{} \ell$, then

$$\exists N \in \mathbb{N}, \forall j \geq N, \left|\frac{x_j}{y_j} - \ell\right| \leq \frac{\ell}{2}.$$

Therefore
$$\frac{x_{j}}{y_{j}}=l+\frac{x_{j}}{y_{j}}-l$$ and thus $$\frac{x_{j}}{y_{j}}\leq l+ | \frac{x_{j}}{y_{j}} - l|$$ so
$$\forall j \geq N, \frac{x_j}{y_j} \leq \ell + \left|\frac{x_j}{y_j} - \ell\right| \leq \frac{3}{2}\ell,$$
and then similarly, 
$$|\frac{x_{j}}{y_{j}}-l| \geq l - \frac{x_{j}}{y_{j}}$$

which rearranges to
$$\forall j \geq N, \frac{x_j}{y_j} \geq \ell - \left|\frac{x_j}{y_j} - \ell\right| \geq \ell - \frac{\ell}{2} = \frac{\ell}{2}.$$

Therefore (from multiplying through),

$$0 \leq x_j \leq \frac{3}{2}\ell y_j, \, \forall j \geq N, \text{ and}$$
(flipping around everything on the line two above)
$$0 \leq y_j \leq \frac{2}{\ell} x_j, \, \forall j \geq N.$$

this gives $\sum_{j=N}^{\infty} x_j$ converges $\iff \sum_{j=N}^{\infty} y_j$ converges and so

$$\sum_{j=0}^{\infty} x_j \text{ converges} \iff \sum_{j=0}^{\infty} y_j \text{ converges}.$$

# Convergence tests for series 
![[The integral test]]
![[The ratio test]]

# Series with signs changing 
![[absolute convergence]]
![[summation by parts]]