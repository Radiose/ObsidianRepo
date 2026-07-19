uniform continuity

This is a specific property of a continuous function defined by the following statement 
$\forall\epsilon\ \exists \delta \ \ s.t\ \ \forall x,y \in A$
$|x-y|<\delta \implies|f(x)-f(a)|<\epsilon$

To rigorously prove, we need a tool to help us to do this. 

Suppose that we have two intervals, $[a,b], \ [b,c]$ with a function $f$ continuous on $[a,c]$. Let $\epsilon >0$ and suppose that the following statements hold 

i) if $x$ and $y$ are in $[a,b]$ and $|x-y|<\delta_{1}$, then $|f(x)-f(y)|<\epsilon$
ii) if $x$ and $y$ are in $[b,c]$ and $|x-y|<\delta_{2}$, then $|f(x)-f(y)|<\epsilon$

We would like to know if there's some $\delta>0$ such that $|f(x)-f(y)|<\epsilon$ whenever $x,y$ are points in $[a,c]$ with $|x-y|<\delta$. It may appear like taking the minimum of $\delta_{1},\delta_{2}$ is a good idea, but this will fail if $\delta_{1}$ is in $[a,b]$ and $\delta_{2}$ is in $[b,c]$. The image below shows this better. 
![[Pasted image 20260719100355.png]]

We use the lemma below to help us 

### Lemma 
Let $a<b<c$ and let $f$ be continuous on the interval $[a,c]$. Let $\epsilon>0$ and suppose that the statements i) and ii) hold. Then, there is a $\delta>0$ such that:
	if $x$ and $y$ are in $[a,c]$, and $|x-y|<\delta$, then $|f(x)-f(y)|<\epsilon$

Proof:
Since $f$ is continuous at $b$, there exists a $\delta_{3}>0$ such that $$|x-y|<\delta_{3} \implies|f(x)-f(b)|< \frac{\epsilon}{2}$$ It follows that $$\text{iii) if }|x-b|<\delta_{3} \text{ and }|y-b|<\delta_{3},\ \text{then }|f(x)-f(y)|<\epsilon$$
We choose $\delta$ to be the minimum of $\delta_{1},\ \delta_{2}\ \delta_{3}$. Thus, all three cases are covered ($x,y$ in $[a,b]$, $[b,c]$, or $x$ in $[a,b]$, $y$ in $[b,c]$)

We use this lemma to prove some statements 
## Theorem 1
if $f$ is [[continuous function|continuous]] on $[a,b]$, then $f$ is *uniformly continuous* on $[a,b]$. 

Proof:
We define the term $\epsilon$-good on $[a,b]$ to mean that there exists a $\delta>0$ such that for all $y,z \in[a,b]$
$$|y-z|<\delta \implies|f(y)-f(z)|<\epsilon$$
We are trying to proof that $f$ is $\epsilon$-good for any $\epsilon>0$. 
Consider any $\epsilon$>0, then let $$A=\{ x:a\leq x\leq b:\ f\text{ is }\epsilon\text{-good on }[a,x] \}$$
Because $A \not=\emptyset$ and is bounded above by $b$, it has a least upper bound $\alpha$. (We should write $\alpha_{\epsilon}$, since it depends on $\epsilon$, but its not super relevant here).
We seek to prove that $\alpha=b$ no matter what $\epsilon$ is.
Suppose that $\alpha<b$. Since $f$ is continuous at $\alpha$, there is some $\delta_{0}>0$ such that $|y-\alpha|<\delta_{0} \implies|f(y)-f(\alpha)|< \frac{\epsilon}{2}$. Consequently, if $|y-\alpha|<\delta$ and $|z-\alpha|<\delta$, then $|f(y)-f(z)|<\epsilon$. 