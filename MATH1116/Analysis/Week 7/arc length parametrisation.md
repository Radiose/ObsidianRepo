---
aliases:
  - parametrisation
---
When integrating along curves, or with [[Definite integral|integral]]s of the form $\int_\mathcal{C}$, its important to establish that that value of the integral is not dependant on the [[vector valued curve]].

That is, if we attempt to describe the unit circle as $\mathcal{C}=\{ \cos(t),\sin(t)|t \in[0,2\pi] \}$, or $\mathcal{C_{2}}=\{ \cos(5t),\sin 5(t)|t\in \mathbb{R} \}$, we need to ensure that $\int_{\mathcal{C}}F(x)=\int_{C_{1}}F(x)$.

If $\mathcal{C}=\{ f(t);t\in[a,b] \}$, then $f:[a,b]\to \mathbb{R}^n$ is called a parametrisation of $\mathcal{C}$

# Definition 
Let $\mathcal{C}=\{  x(t);t \in[a,b]\}$ with $x:[a,b]\to \mathbb{R}^n$ be [[multivariate differentiability|differentiable]], and $\lVert x'(t) \rVert\not=0\ \forall t\in[a,b]$.

Define $y(t):=x(a+t(b-a)),\ \ \forall t \in[0,1]$, we have $\mathcal{C}=\{ y(t);t\in[0,1] \}$

Define $\sigma(t):=\int_{0}^t \lVert y'(s) \rVert ds\quad \forall t\in[0,1]$

Note that $\sigma$ is increasing from $[0,1]$, to $[0,\sigma(1)]$, so it is a [[Bijective|bijection]].
Finally, we have that $$\mathcal{C}=\{ y(\sigma^{-1}(s));s \in[0,\sigma(1)] \}$$ 
We call $z:[0,\sigma(1)]\to \mathbb{R}^n$
	$s \mapsto y(\sigma^{-1}(s)))$ the [[arc length parametrisation]] of $\mathcal{C}$

# Proposition 
Let $\mathcal{C}=\{ x(t);t\in[a,b] \}$ and $z:[0,\sigma(1)]$ be its [[arc length parametrisation]]. 
Let $F:\mathbb{R}^n \to \mathbb{R}^n$ and $f:\mathbb{R}^n \to \mathbb{R}$ be such that $t \mapsto F(x(t))$ and $t\mapsto f(x(t))$ are [[continuous function|continuous]] on $[a,b]$.

Then, $$\int_{x(t);t\in[a,b]}F(x)\cdot dx=\int_{z(s);s \in[0,\sigma(1)]}F(x)\cdot dx$$and $$\int_{x(t);t\in[a,b]}f(x)dx=\int_{z(s);s \in[0,\sigma(1)]}f(x)dx$$
### Proof 
We define $y(t):=x(a+t(b-a))$ and $\sigma(t):=\int_{0}^t \lVert y'(s) \rVert ds$ for all $t\in[0,1]$

Note that since $\sigma^{-1}(\sigma(s))=s$, $(\sigma^{-1})'(t)= \frac{1}{\sigma'(\sigma^{-1}(t))}=\frac{1}{\lVert y'(\sigma^{-1}t) \rVert}$ for all $t\in[0,\sigma(1)]$ ([[Inverse function|proof]] for the first one, and FTC for the denominator of second third ).
So, for $s \in[0,\sigma(1)]$ $z'(s)=\frac{1}{\sigma'(\sigma^{{-1}}(s))}\cdot y'(\sigma^{-1}(s))=\frac{ y'(\sigma^{-1}(s)) }{\lVert y'(\sigma^{-1}(s)) \rVert}$. 

Thus,$$
\begin{aligned}
\int_{\{z(s)\, s\in[0,\sigma(1)]\}} F(x)\cdot dx
&= \int_0^{\sigma(1)} F\big(y(\sigma^{-1}(s))\big)\,\frac{y'(\sigma^{-1}(s))}{\sigma'(\sigma^{-1}(s))}\,ds \text{ via change of variable }\\
&= \int_0^1 F(y(\tau))\,y'(\tau)\,d\tau \text{via another change of var} \\
&= \int_0^1 F\big(x(a+\tau(b-a))\big)(b-a)\,x'\big(a+\tau(b-a)\big)\,d\tau \text{   COV} \\
&= \int_a^b F(x(t))\,x'(t)\,dt
= \int_{\{x(t);\,t\in[a,b]\}} F(x)\cdot dx.
\end{aligned}$$
A similar proof applies for $f(x) \blacksquare$
