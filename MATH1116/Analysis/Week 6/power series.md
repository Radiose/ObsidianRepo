power [[series]]
# Motivation 
Recall that 
$$\ln(1+x)=\int_{0}^1 \frac{1}{1+t}dt=\int_{0}^x \sum_{n=0} ^\infty(-t)^n dt$$
Because this is an infinite sum, we need [[uniform convergence and L1 norm convergence of sequence of functions|uniform convergence]] to transfer the sum out of the integral. 
Let $x \in[0,1)$ Define $\forall n \in \mathbb{N},\ \forall t\in[0,x]\ \ f_{n}(t):=(-t)^n$
$||f_{n}||_{\infty}=sup_{t\in[0,x]}f_{n}(t):= |-t|^n=x^n$
$\sum_{n=1}^\infty x^n$ converges, thus $\sum_{n=0}^\infty ||f_{n||_{\infty}}$ converges. 
$\implies \sum_{n=0}^\infty f_{n}$ converges uniformly (via [[uniform convergence of a series of sequence of functions#Theorem|this theorem]]). 

Thus, $$\int_{0}^1 \sum_{n=0}^\infty (-t)^ndt=\sum_{n=0}^\infty \int_{0}^1(-t)^ndt=\sum_{n=0}^\infty (-1)^n \frac{x^{n+1}}{n+1}$$
# Definition 
let $(a_{n})_{n \in\mathbb{N}}\in \mathbb{R}^\mathbb{N}$. Let $c \in \mathbb{R}$
Define $f_{n}:\mathbb{R}\to \mathbb{R}$
	$x \mapsto a_{n}(x-c)^n$
The series of functions $\sum_{n=0}^\infty f_{n}$ is called a [[power series]] centred at $0$. 
As an abuse of notation, we write $\sum_{n=0}^\infty a_{n}(x-c)^n$

# Lemma 

Let $(a_{n})_{n \in \mathbb{N}} \in \mathbb{R}^\mathbb{N}$. Let $c \in \mathbb{R}$.
Assume $\exists x \in \mathbb{R}  \setminus \{c\}: \sum{a_{n}}(x-c)^n$ converges. 
Then, $\forall r \in(0, |x-c|)\sum a_{n}r^n$ converges. 

### Proof 
Since $\sum_{n=0}^\infty a_{n}(x-c)^n$ converges, $a_{n}(x-c)^n \xrightarrow[n \to \infty]{}0$
let $R \in(0,|x-c|)$, thus
$$\exists N \in \mathbb{N}\quad \forall n \geq N|a_{n}R^n|=|\frac{R}{x-c}|^n \cdot |a_{n}(x-c)^n|$$
$$\leq \left( \frac{R}{|x-c|} \right)^n$$
Since $\sum \left( \frac{R}{|x-c|} \right)^n$ converges, so does $\sum(a_{n} |R^n|)$


# Theorem 
Let $(a_{n})_{n  \in \mathbb{N}} \in \mathbb{R}^\mathbb{N} \quad c \in \mathbb{R}$
One of the following holds:
$(1)\quad \forall x \in \mathbb{R} \setminus \{ c \}\quad \sum_{n=0}^\infty a_{n}(x-c)^n$ diverges 

$(2)\quad \forall x \in \mathbb{R} \setminus \{ c \} \sum_{n=0}^\infty a_{n}(x-c)^n$ converges 

$(3)\quad \exists \delta >0:\forall x \in \mathbb{R} \setminus \{ c \}$
- $|x-c| < \delta \implies \sum_{n=0}^\infty a_{n}(x-c)^n$ converges 
- $|x-c|>\delta \implies \sum_{n=0}^\infty a_{n}(x-c)^n$ diverges  

### Proof 
Assume that neither $(1)$ or $(2)$ holds. 
Then, $\exists x_{0}\in \mathbb{R} \setminus \{ c \}:\quad \sum {a_{n}}(x_{0}-c)^n$ converges 
$\quad \quad \ \ \  \exists x_{1} \in \mathbb{R} \setminus \{ c \}:\quad \sum{|a_{n}|} |x_{1}-c|^n$ diverges 
By the lemma above 
if $R < |x_{0}-c|$, then $\sum |a_{n}R|$ converges.
