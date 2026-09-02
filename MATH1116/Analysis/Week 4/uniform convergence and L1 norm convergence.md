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
\left| \int_a^b f_n(x)\,dx - \int_a^b f(x)\,dx \right| \leq \left| \int_{a}^b sup_{y \in[a,b]}|f_{n}(y)-f(y)|\right| =(b-a)\|f_n - f\|_\infty.
$$

Therefore,

$$
\left| \int_a^b f_n(x)\,dx - \int_a^b f(x)\,dx \right| \leq \min\big(\|f_n - f\|_1,\ (b-a)\|f_n - f\|_\infty\big),
$$

and thus tends to $0$ as $n$ tends to infinity. $\blacksquare$



# Important remark 
$||f_{n}(x)-f(x)|| \xrightarrow[n \to \infty]{}0$
$\iff \forall\epsilon>0\quad  \exists N \in \mathbb{N} \quad \forall n >N \ \  sup_{x \in[a,b]} |f_{n}(x)-f(x)|<\epsilon$
$\iff \forall\epsilon>0 \quad \exists N \in \mathbb{N} \quad \forall x \in[a,b]\ \ |f_{n}(x)-f(x)|<\epsilon$
$\implies \forall x \in[a,b]\ \ \forall\epsilon>0\ \ \exists M_{\epsilon,x}\forall n\geq M\ \ |f_{n}(x)-f(x)|<\epsilon$
$\implies f_{n}(x)\xrightarrow[n \to \infty]{}f(x)$ pointwise. 

As you can see, the difference between pointwise and uniform convergence is the same as [[continuous function|continuous]] vs [[uniform continuity]], IE whether $N$ depends on $x$ or not. 


# Theorem 2
let $b >a$. Let $f_{n}:[a,b]\to \mathbb{R}$, and $f:[a,b) \to\mathbb{R} \ \ \forall n \in \mathbb{N}$.
If $f_{n}\in C[a,b]\ \ \ \forall n\in \mathbb{N},$ and $||f_{n}(x)-f||_{\infty}\to {0}$, then $f \in C[a,b]$.
(a uniformly convergent, continuous sequence of functions must converge to a continuous function)
### Proof 
Let $\epsilon>0$, $x \in[a,b]$. Pick $N\in \mathbb{N} :||f_{n}-f||_{\infty}<\epsilon\ \ \forall n\in \mathbb{N}$ 
Since $f_{N} \in C[a,b]$ $\forall x \in[a,b]$, then $\exists\delta>0$: $$\forall y \in[a,b]|y-x|<\delta \implies$$