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

# Theorem 
Let $(a_{n})_{n  \in \mathbb{N}} \in \mathbb{R}^\mathbb{N} \quad c \in \mathbb{R}$
One of the following holds:
$(1)\quad \forall x \in \mathbb{R} \setminus \{ c \}\quad \sum_{n=0}^\infty a_{n}(x-c)^n$ diverges 

$(2)\quad \forall x \in \mathbb{R} \setminus \{ c \} \sum_{n=0}^\infty a_{n}(x-c)^n$ converges 

$(3)\quad \exists \delta >0:\forall x \in \mathbb{R} \setminus \{ c \}$
- $|x-c| < \delta \implies \sum_{n=0}^\infty a_{n}(x-c)^n$ converges 
- $|x-c|>\delta \implies \sum_{n=0}^\infty a_{n}(x-c)^n$ diverges  

### Proof 
Assume $\exists x_{0}\in \mathbb{R} \setminus \{ c \}$ such that $\sum_{n=0}^\infty a_{n}(x_{0}-c)^n$ converges. If not, (1) holds.
We have $a_{n}(x_{0}-c)^n \xrightarrow[n \to \infty]{}0$
Therefore, $\exists N >0$ such that $\forall n \in \mathbb{N}$, $|a_{n}(x_{0}-c)^n|\leq M$ and thus $\forall n\in \mathbb{N},\ \forall x \in \mathbb{R}$, $|a_{n}(x-c)|\leq M \left( \frac{|x-c|}{|x_{0}-c|} \right)^n$
Therefore, $|x-c|<|x_{0}-c|$ implies that the M term goes to zero, and via [[Convergence of series#Theorem 2 (converging series bounds smaller one)|comparison test]], $\sum a_{n}(x-c)^n$ must converge, so $\sum |a_{n}r_{0}^n|$ converging implies that $\sum |a_{n}r^n|$ converges for all $r \in[0,r_{0}]$
If $\sum^\infty a_nr^n$ converges for all $r\geq0$, then $(2)$ holds. 
If note, let $\delta:= sup \left\{  r>0:\sum_{n=0}^\infty |a_{n}r^n|  \text{  converges}\right\}$

Then, $\forall x \in(c-\delta,c+\delta),\quad\exists r\in(0,\delta)$ such that $|x-c|=r<\delta$

Therefore, $\forall x \in(c-\delta,c+\delta),\sum_{n=0}^\infty a_{n}(x-c)^n$ converges. 

 $\forall x \not \in [c-\delta,c+\delta]$$\quad \exists R>\delta$ such that $|x-c|=R$. Assume that $\sum_{n=0}^\infty a_{n}(x-c)^n$ converges. Then, $\sum_{n=0}^\infty a_{n}\bar{R}^{n}$ converges for $\delta<\bar{R}<R$, which contradicts the definition of $\delta$. Thus, $(3)$ holds $\blacksquare$.

