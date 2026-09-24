Let $f$ be a function $\mathbb{R}\to \mathbb{R}^n$
We say $f$ is [[derivative|differentiable]] at $t \in \mathbb{R}$ if the folllowing hold:
$$\exists \ell \in \mathbb{R}^n\quad\forall\epsilon>0\quad\exists\delta>0\quad\forall h\in \mathbb{R}$$
$$\lvert h \rvert<\delta \implies \left\lVert  \frac{1}{h}\left[ f(t +h)-f(t) \right]-\ell  \right\rVert<\epsilon$$
We write $\lim_{ h \to \infty } \frac{1}{h} \left[ f(t+h)-f(t) \right]=\ell$

# Theorem 1
Let $f:\mathbb{R}\to \mathbb{R}^n$
Define $x_{j}:\mathbb{R}\to \mathbb{R}$
	$t \mapsto f(t)\cdot x_{j}$
$f$ is [[derivative|differentiable]] at $t \in \mathbb{R}$ if and only if $x_{j}$ is differentiable at $t \in \mathbb{R}$
Moreover, $f'(t)=(x_{1}'(t)\cdot e_{1},x_{2}'(t)\cdot e_{2},\dots,x_{n}'(t)\cdot e_{n})$

# Theorem 2
Let $f,g:\mathbb{R}\to \mathbb{R}^n$ be differentiable at $t\in \mathbb{R}$. Then, $$(f\cdot g)'(t)=f'(t)\cdot g(t)+f(t)\cdot g'(t)$$
