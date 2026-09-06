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

# Theorem 2(ratio determines radius of convergence)
Let $(a_{n})_{n\in \mathbb{N}} \in \mathbb{R}^\mathbb{N},c \in \mathbb{R}$
$(1)$ If $$\lim_{ n \to \infty }\frac{a_{n+1}}{a_{n}}=\ell>0$$
then $\sum a_{_{n}}(x-c)^n$ has radius of convergence of $\frac{1}{\ell}$

$(2)$ If $$\lim_{ n \to \infty } \left| \frac{a_{n+1}}{a_{n}}\right|=0$$ then $\sum {a_{n}}(x-c)^n$ has radius of convergence $\infty$

$(3)$ If $$\lim_{ n \to \infty }\left| \frac{a_{n+1}}{a_{n}}\right|=\infty$$then $\sum a_{n}(x-c)^n$ has radius of convergence of $0$.

### Proof 
$(1)$
$\forall x \in \mathbb{R} \setminus \{ c \}$
$$\lim_{ n \to \infty } \left| \frac{a_{n+1} (x-c)^{n+1}}{a_{n}(x-c)^n} \right| =\ell|x-c|$$
Via [[The ratio test]], $\ell \cdot|x-c|$ will converge $\iff \ell \cdot|x-c|<1$
$\implies |x-c|  < \frac{1}{\ell}$.
Similarly, $\ell \cdot|x-c|$ will diverge $\iff l\cdot|x-c|>1$
$\implies |x-c|> \frac{1}{\ell}$
This is the definition of $\delta$ from [[power series#Theorem|theorem 1]].
 
$(2)$
$$\lim_{ n \to \infty } \left| \frac{a_{n+1} (x-c)^{n+1}}{a_{n}(x-c)^n} \right| =0|x-c| ={0}\ \ \forall x \in \mathbb{R}$$

$\implies \sum a_{n} (x-r)^n$ converges for all $x$ via ratio test. 

$(3)$
$$\lim_{ n \to \infty } \left| \frac{a_{n+1} (x-c)^{n+1}}{a_{n}(x-c)^n} \right| =\infty|x-c|=\infty >1$$
$\implies \sum a_{n}(x-c)^n$ diverges $\forall x \in \mathbb{R}$ via ratio test. 

# Remark 
Let $(a_{n})_{n\in \mathbb{N}},(b_{n})_{n\in \mathbb{N}}\in \mathbb{R}^\mathbb{N}$.
If $\sum a_{n}(x-c)^n$ has radius of convergence of $\delta$, and $\sum b_{n}(x-c)^n$ has radius of convergence of $\gamma$, then $\sum(a_{n}+b_{n})(x-c)^n$ has radius of convergence of at least $\min(\gamma,\delta)$. (if no cancellation occurs between $a_{n}$ and $b_{n}$, then it will be minimum, but it would be larger if cancellation occurs).

# Theorem 3 
Let $\sum a_{n}(x-c)^n$ have radius of convergence $r$.
Then, $\sum \frac{a_{n}}{n+1}(x-c)^{n+1}$ has radius of convergence of $r$.
Additionally, $\forall x \in (c-r,c+r)$, 
$$\int_{0}^x \sum a_{n}(t-c)^n dt=\sum \frac{a_{n}}{n+1}(x-c)^{n+1}$$
### Proof 
let $x \in(c-r, c+r)$, $n \in \mathbb{N}$
$\left| \frac{a_{n}}{{n+1}} (x-c)^{n+1}\right| \leq |a_{n}(x-c)^{n}| \cdot \left| x-c \right|$
Since $\sum a_{n}(x-c)^n$ converges, via comparison test, so does $\sum \frac{a_{n}}{n+1}(x-c)^n$
Therefore, radius of convergence is $\bar{r} \geq r$.
Let $\bar{\rho} > \rho >r$. Then there exists $N \in \mathbb{N}$ such that $\forall n \geq N$
$\left| \frac{a_{n}}{n+1} \bar{\rho}^n\right|=|a_{n}\rho^n| \left( \frac{\bar{\rho}}{\rho} \right)^n \cdot \frac{1}{n+1} \geq |a_{n}\rho^n|$ ($\bar{\rho}^n$ grows quicker than $\frac{1}{n}$). Thus, because $\sum a_{n}\rho_{n}$ diverges (by definition of $r$), then, $\sum a_{n}\bar{\rho}_{_{n}}$ will as well. Thus,  $\sum a_{n}\bar{\rho}_{_{n}}$ will diverge for $\bar{\rho} > r$, thus $\bar{r} \leq r$. 



Let $x \in(c,c+r)$, $N \in \mathbb{N}$, $\delta \in(x-c,r)$
Then $$\left| \int_{c}^x \sum_{n=0}^N a_{n}(t-c)^ndt-\sum_{n=0}^N\int_{c}^x a_{n}(t-c)^ndt \right|\leq \int_{c}^x \left| \sum_{n=N+1}^\infty a_{n}(t-c)^n\right|dt  $$
$$\leq \int_{c}^x \sum_{n=N+1}^\infty |a_{n}||\delta|^n dt$$
$$=(x-c)\sum_{n=N+1}^\infty |a_{n}\delta^n|\xrightarrow[n \to \infty]{}0$$(because the series above converges, its tail converges to $0\blacksquare$).
A similar argument applies for $x \in(c-r,c)$
# Theorem 4 
Let $(a_{n})_{n \in \mathbb{N}} \in \mathbb{R}^\mathbb{N}$, $c \in \mathbb{R}$, $r$ be the radius of convergence of $\sum a_{n}(x-c)^n$. Then 
$(1)$ $$\sum_{{n=0}}^\infty (n+{1}) a_{n+1}(x-c)^n$$has radius of convergence $r$
$(2)$ $$f: x \mapsto \sum_{n=0}^\infty a_{n}(x-c)^n$$
is [[derivative|differentiable]] on $(c-r,c+r)$ and $$f'(x)=\sum_{n=0}^\infty (n+1)a_{n+1}(x-c)^n$$
### Proof 
$(1)$:
Let $r>0$. For all $n \in \mathbb{N}^*$, $|na_{n}r^{n-1}|\geq|a_{n}r^{n-1}|$. Therefore the radius of convergence of $\bar{r}$ of $\sum_{n=0}^\infty (n+1)a_{n+1}(x-c)^n$ is such that $\bar{r} \leq r$. Basically, if $a_{n}r^{n-1}$ diverges, then the other one has to as well. 

Let $0<\bar{\rho}<\rho<r\quad \forall n\in \mathbb{N}$ $$\left| na_{n} \bar{\rho} ^{n-1}\right|\leq \frac{1}{\rho}|a_{n}\rho^n|{n} \cdot \left( \frac{\bar{\rho}}{\rho} \right) ^n $$
$\exists N\in \mathbb{N}$ such that $\forall n\geq N$
$$|na_{n}\bar{\rho}^{n-1}|\leq \frac{1}{\rho}|a_{n}\rho^n|$$
