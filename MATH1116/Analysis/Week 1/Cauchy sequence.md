---
aliases:
  - cauchy
---
# Theorem
A [[Sequence]] [[Convergence of a sequence|converge]]s if and only if it is Cauchy. I.E
$\forall \epsilon>0 \ \ \ \exists N \in \mathbb{N}\ \ \ \forall n,m>N\ \ |x_{n}-x_{m}|<\epsilon$

This theorem is treated as an axiom in construction of the [[real number|reals]]. 


Axiom: Let $(x_{n})_{n \in \mathbb{N}}\in \mathbb{R}^\mathbb{N}$ be non decreasing and bounded, then $x_{n}$ [[Convergence of a sequence|converge]]s. 

Proof:
$[\implies]$ Assume $(x_{n})_{n \in \mathbb{N}}$ converges, that is $\forall\epsilon>0 \ \ \exists N \in \mathbb{N}\ \ \forall n>N\ \ |x_{n}-L|<\epsilon$

Then $\exists N \in \mathbb{N}\ \ \forall n\geq N\ \ |x_{n}-L|< \frac{\epsilon}{2}$, therefore $\forall n,m \geq N\ \ |x_{n}-x_{m}|\leq|x_{n}-l|+|l-x_{m}|<\epsilon$


$[\impliedby]$ (the challenge with this direction is that its hard to prove that they converge to some actual point rather than just being together forever).

Assume that $(x_n)_{n \in \mathbb{N}}$ is Cauchy. Then $\exists N \in \mathbb{N}$ such that $\forall n \ge N, |x_n - x_N| \le 1$. Therefore
$$x_{n}=(x_{n}-x_{\bar{N}})+x_{\bar{N}}\leq |x_{n}-x_{N}|+|x_{N}|<1+|x_{\bar{N}}|$$
$$\therefore \forall n \ge N, \quad |x_n| \le |x_n - x_N| + |x_N| \le 1 + |x_N|.$$

$$\forall n \in \mathbb{N}, \quad |x_n| \le 1 + \max_{0 \le k \le N} |x_k|.$$
(maximum of the sequence is either N or something before it)
Therefore $(x_n)_{n \in \mathbb{N}}$ is a bounded sequence.

Let $y_n = \sup_{k \ge n} x_k, \forall n \in \mathbb{N}$. Then $(-y_n)_{n \in \mathbb{N}}$ is bounded and nondecreasing.
(if L is what -y converges to, then y must converge to -L)

Let $\bar\ell = \lim_{n \to \infty} y_n$.

Let $z_n = \inf_{k \ge n} x_k, \forall n \in \mathbb{N}$. Then $(z_n)_{n \in \mathbb{N}}$ is bounded and nondecreasing.

Let $\underline\ell = \lim_{n \to \infty} z_n$.

Let $\varepsilon > 0$. Then $\exists N \in \mathbb{N}, \forall n, m \ge N, |x_n - x_m| < \dfrac{\varepsilon}{5}$ and $|y_N - \bar\ell| < \dfrac{\varepsilon}{5}, |z_n - \underline\ell| < \dfrac{\varepsilon}{5}$.

Moreover

$$\exists k \ge N, \quad |y_N - x_k| < \frac{\varepsilon}{5}$$
(after N, there is some $x_{k}$ close to the inf/sup of $x_{n},x_{n+1}\dots$)
$$\exists j \ge N, \quad |z_n - x_j| < \frac{\varepsilon}{5}.$$

Therefore

$$|\underline\ell - \bar\ell| \le |\underline\ell - z_N| + |z_N - x_j| + |x_j - x_k| + |x_k - y_N| + |y_N - \bar\ell| < \varepsilon.$$

This gives $\underline\ell = \bar\ell$. Let $\ell = \bar\ell$. Then

$$\forall n \ge k, \quad |x_n - \ell| \le |x_n - x_k| + |x_k - y_N| + |y_N - \ell| < \frac{3\varepsilon}{5} < \varepsilon.$$

Therefore $x_n \xrightarrow[n \to +\infty]{} \ell$. $\blacksquare$

## Flawed lecture proof
Assume $(x_{n})_{n \in \mathbb{N}}$ is Cauchy. IE, $\forall\epsilon>0\quad \exists N \in \mathbb{N}\quad \forall n>m>N |x_{n}-x_{m}|< \frac{\epsilon}{3}$

Define $(y_{n})_{n \in \mathbb{N}}\in \mathbb{R}^\mathbb{N}$ by $y_{n}=inf_{\ k\geq n}\ x_{k}$, that is, the greatest lower bound of all $x_{k}$ when $k \geq n$.

Remark: $y_{n+1}\geq y_{n}\ \ \ \ \forall n \in \mathbb{N}$ - either the greatest lower bound is the same, or its nondecreasing (the set is getting smaller).

By the definition of Cauchy, we know that with $\epsilon =1\ \exists \bar{N}\ \ \forall n>\bar{N}\ \ |x_{n}-x_{\bar{N}}|<1$
Thus via some quick inequalities, (we add the $x_{\bar{N}}$ term at the end to match the Cauchy def)

$x_{n}=(x_{n}-x_{\bar{N}})+x_{\bar{N}}\leq |x_{n}-x_{N}|+|x_{N}|<1+|x_{\bar{N}}|$

Thus,  $\forall n \in \mathbb{N}$      $|x_{n}|<1+ \underset{0 \leq k\leq \bar{N}}{max} |x_{k}|$ - if we did not do this, then there's no proof that this sequence is bounded. We have proven that $\forall n \geq \bar{N}$ we are bounded, and thus there's some bound before that (there's only a finite number of terms). 
Therefore, $x_{n}$ is bounded. 
Also, $\forall n \in \mathbb{N} \ y_{n}< \underset{ 0\leq k\leq \bar{N} }{ max }$
Because $y_{n}$ is is bound, and nondecreasing via the axiom it must **converge**. Let $l :=\lim_{ n \to \infty }y_{n}$
We have that $\forall\epsilon>0$ $\exists M\geq \bar{N}$  $\forall n \geq M$  $|y_{n}-l|< \frac{\epsilon}{3}$

Since $y_{n}=\underset{ k\geq n }{ inf }\ x_{k} \ \ \ \forall n \in \mathbb{N}$
we have that $\forall\epsilon>0\quad \forall n \in \mathbb{N} \quad \exists k_{n}\geq n \quad |x_{k}-y_{n}|< \frac{\epsilon}{3}$. Basically, for any epsilon and any greatest lower bound indexed by $n$, there is some $x_{k}$ after that that will be closer to the lower bound than that epsilon. 

Combining the three statements, we get $\forall\epsilon>0 \quad \exists N_{0}\geq max(\bar{N}, k_{(\bar{N})})\quad \forall n\geq N_{0}$ 
$$|x_{n}-l|\leq|x_{n}-x_{k}|+|x_{k}-y_{n}|+|y_{n}-l|< \frac{\epsilon}{3} \times 3 = \epsilon$$

# Proving arbitrary sequences converge using [[Cauchy sequence|cauchy]] 

One very important application of Cauchy is to be able to show that arbitrary sequences converge. 
