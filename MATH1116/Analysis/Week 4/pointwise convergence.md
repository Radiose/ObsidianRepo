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
