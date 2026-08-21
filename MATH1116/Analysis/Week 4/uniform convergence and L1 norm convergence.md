---
aliases:
  - uniform convergence
  - L1 norm
  - converges uniformly
---
let $b>a$, let $f :[a,b]\to \mathbb{R},\quad f_{n}:[a,b]\to \mathbb{R}\ \ \forall n \in \mathbb{N}$
We say that $(f_{n})_{n \in \mathbb{N}}$ **converges uniformly** to $f$ if:
$$||f-f_{\infty}||:= sup_{x \in[a,b]}|f_{n}(x)-f(x)|\xrightarrow[n \to \infty]{}0$$
Additionally, when $f$, $f_{n}$ are [[Integrable (spivak)|integrable]], we say that $f_{n}$ converges to  $f$ in $L_{1}$ norm if $||f-f_{m}||:= \int_{a}^b |f(x)-f_{n}(x)dx| \xrightarrow[n \to \infty]{}0$

### Use
The point of these are that they fix some of the [[pointwise convergence#Some important properties of pointwise convergence|issues]] with [[pointwise convergence]]. 

# Theorem 
*Let $b > a$. Let $f : [a,b] \to \mathbb{R}$ and $f_n : [a,b] \to \mathbb{R}$ be integrable for all $n \in \mathbb{N}$. If $(f_n)_{n\in\mathbb{N}}$ converges to $f$ uniformly or in $L^1$ norm, then*

$$
\lim_{n\to\infty} \int_a^b f_n(x)\,dx = \int_a^b f(x)\,dx
$$

*Proof.* We have that

$$
\left| \int_a^b f_n(x)\,dx - \int_a^b f(x)\,dx \right| =\left|\int_{a}^b f_{n}(x)-f(x)dx\right|\leq \int_a^b |f_n(x) - f(x)|\,dx = \|f_n - f\|_1.
$$

Moreover,

$$
\left| \int_a^b f_n(x)\,dx - \int_a^b f(x)\,dx \right| \leq \left| \int_{a}^b sup_{y \in[a,b]}|f_{n}(y)-f(y)|\right| (b-a)\|f_n - f\|_\infty.
$$

Therefore,

$$
\left| \int_a^b f_n(x)\,dx - \int_a^b f(x)\,dx \right| \leq \min\big(\|f_n - f\|_1,\ (b-a)\|f_n - f\|_\infty\big),
$$

and thus tends to $0$ as $n$ tends to infinity. $\blacksquare$