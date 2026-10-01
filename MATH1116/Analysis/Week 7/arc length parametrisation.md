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
	