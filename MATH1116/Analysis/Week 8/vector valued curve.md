---
aliases:
  - curve
  - unit tangent vector
  - magnitude of curvature
  - length of curve
---
A curve in $\mathbb{R}^n$ is a set of the form $\{ x(t) ;t\in[a,b]\}$, where $a,b\in \mathbb{R}$, and $x:[a,b]\to \mathbb{R}^n$

# Definitions 
Let $a,b \in \mathbb{R}$, $x:[a,b]- >\mathbb{R}^n$ be ${C}^2$ and $\mathcal{C}=\{ x(t);t \in[a,b] \}$. We define $$\lvert C \rvert :=\int_{a}^b \lVert f'(t) \rVert dt $$ as the length of $\mathcal{C}$. 
Let $z$ be the [[arc length parametrisation]] of $\mathcal{C}$. 
For $s \in[0, |\mathcal{C}|]$, we call $z'(s)$ the unit tangent [[vector]] to $\mathcal{C}$ at point $z(s)$,
and $\lVert z''(s) \rVert$ [[The magnitude of a vector|magnitude]] of curvature of $\mathcal{C}$ at point $z(s)$.

### Remark 
$$\sigma(1)=\int_{0}^{\sigma(1)} \lVert z'(s) \rVert ds$$
$$= \int_{0}^{\sigma(1)} \lVert y'(\sigma^{-1}(s)) \rVert (\sigma^{-1})'(s)ds$$
$$= \int_{0}^1 \lVert y'(t) \rVert dt = \int_{0}^1 \lVert (b-a)x'(a+t(b-a)) \rVert dt$$
$$= \int_{a}^b \lVert x'(t) \rVert dt=\lvert \mathcal{C} \rvert$$
So the length of the curve computed by $x$ is the same as using $y$, which is the same as if it was computed using $z$.

