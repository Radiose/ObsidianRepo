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
# Theorem 3 
Let $f,g$ : $\mathbb{R}\to \mathbb{R}^n$ be differentiable at $t \in \mathbb{R}$
define $h:\mathbb{R}\to \mathbb{R}$
	$t \mapsto \left< f(t),g(t) \right>$

Then, $h$ is differentiable at $t$ and $h'(t)= \left< f'(t),g(t) \right> + \left< f(t),g'(t) \right>$


# Theorem 4 
let $g : \mathbb{R} \to \mathbb{R}$ be differentiable at $x \in \mathbb{R}$
let $f:\mathbb{R}\to \mathbb{R}^n$ be differentiable at $g(x)$
Define $F:\mathbb{R}\to \mathbb{R}^n$
	$y \mapsto f(g(y))$
Then, $F$ is differentiable at $x$ and $F'(x)=g'(x)f'(g(x))$
### Proof 
we have that 
$\forall \epsilon > 0\quad \exists\delta_{\epsilon} > 0 \quad\forall h \in \mathbb{R}^*$ 
$\lvert h \rvert<\delta_{\epsilon}\implies \lvert \left[ g(x+h)-g(x) \right]-h(g'(x)) \rvert<\epsilon \cdot h$
and 
$\forall\epsilon>0\quad \exists \eta>0\quad \forall h \in \mathbb{R}$
$\lvert h \rvert<\eta \implies \lVert \left[ f(g(x+h))-f(g(x)) \right]-hf'(y(x)) \rVert<\epsilon \cdot h$

Now, let $\epsilon >0$, let $h \in \mathbb{R}^*:\lvert g(x+h)-g(x) \rvert<\epsilon$
$\left\lVert  \frac{1}{h} \left[ F(x+h)-F(x) \right]-g'(x)-f'(g(x))  \right\rVert$
$= \left\lVert   \frac{1}{h} \left[ f( g(x)+g(x+h) -g(x) -f(g(x))\right] -g'(x)f'(g(x)) \right\rVert$
$\leq \left\lVert  \frac{1}{h}[g(x+h)-g(x)]f'(g(x))-g'(x)f'(g(x))  \right\rVert$