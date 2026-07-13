# Proving with the axiom 
We define the set $A$ as follows:
$A = \{ x : a \le x \le b, \text{ and }f\text{ is negative on the interval }[a,x] \}$
![[Pasted image 20260712185730.png]]
Clearly, $A \not= \emptyset$, since $a$ is in $A$; in fact, there is some $\delta > 0$ such that $A$ contains all points $x$ satisfying $a\le x < a+\delta$. This follows since $f$ is [[continuous function|continuous]] on $[a,b]$ and $f(a)<0$. Similarly, $b$ is an upper bound for $A$, and there is a $\delta>0$ such that all points $x$ satisfying $b-\delta<x\le b$ are upper bounds for $A$. 

From these remarks, it follows that A has a [[Completeness axiom|supremum]] $\alpha$ and that $a<\alpha<b$. 
We wish to show that $f(\alpha)=0$ via eliminating possibilities $f(\alpha)<0$ and $f(\alpha)>0$. 



Suppose first that $f(\alpha) < 0$. By Theorem 6, there is a $\delta > 0$ such that $f(x) < 0$ for $\alpha - \delta < x < \alpha + \delta$ (Figure 2). Now there is some number $x_0$ in $A$ which satisfies $\alpha - \delta < x_0 < \alpha$ (because otherwise $\alpha$ would not be the *least* upper bound of $A$). This means that $f$ is negative on the whole interval $[a, x_0]$. But if $x_1$ is a number between $\alpha$ and $\alpha + \delta$, then $f$ is also negative on the whole interval $[x_0, x_1]$. Therefore $f$ is negative on the interval $[a, x_1]$, so $x_1$ is in $A$. But this contradicts the fact that $\alpha$ is an upper bound for $A$; our original assumption that $f(\alpha) < 0$ must be false. 


Suppose, on the other hand, that $f(\alpha) > 0$. Then there is a number $\delta > 0$ such that $f(x) > 0$ for $\alpha - \delta < x < \alpha + \delta$.
Once again we know that there is an $x_0$ in $A$ satisfying $\alpha - \delta < x_0 < \alpha$; but this means that $f$ is negative on $[a, x_0]$, which is impossible, since $f(x_0) > 0$. Thus the assumption $f(\alpha) > 0$ also leads to a contradiction, leaving $f(\alpha) = 0$ as the only possible alternative.



## More theorems based off the axiom 
Theorem 1:

If $f$ is continuous at $a$, then there is a number $\delta > 0$ such that $f$ is bounded above on the interval $(a-\delta, a+\delta)$.

proof: 
Since $\lim_{ x \to a } f(x)=f(a)$, then using [[The formal definition of a limit]], $$\forall\epsilon>0 \ \ \ \exists\delta\ \ \ \ s.t\ \ \ 0<|x-a|<\delta \implies|f(x)-f(a)|<\epsilon$$
Thus, $f$ is bounded above by $f(a)+\epsilon$

# Proof of the binding of f using axioms 

If $f$ is continuous on $[a,b]$, then $f$ is bounded above. 

Proof: 
Let $A =\{ x: a \le x \le b| \text{ and }f \text{ is bounded above on }[a,x] \}$
Clearly A is not empty, and $A$ is bounded above by $b$, so $A$ has a [[Completeness axiom|least upper bound]] $\alpha$. 

We prove that $\alpha = b$
Suppose instead that $\alpha <b$. By theorem 1, there is $\delta > 0$ such that $f$ is bounded on $(\alpha-\delta, \alpha+\delta)$. Since $\alpha$ is the least upper bound, there is some $x_{0}\in A$ satisfying $\alpha-\delta<x_{0}<\alpha$. This means that $f$ is bounded on $[a,x_{0}]$. 

But if $x_{1}$ is any number such that $a< x_{1}<\alpha+\delta$, then $f$ is bounded on $[x_{0},x_{1}]$. Therefore, $f$ is bounded on $[a,x_{1}]$ so $x_{1}$ is in $A$, contradicting the fact that $\alpha$ is an upper bound for $A$. This shows that $\alpha = b$. 

One detail should be mentioned: this demonstration implicitly assumed that $a < \alpha$ \[so that $f$ would be defined on some interval $(\alpha - \delta, \alpha + \delta)$] ; the possibility $a = \alpha$ can be ruled out similarly, using the existence of a $\delta > 0$ such that $f$ is bounded on $\{x : a \leq x < a + \delta\}$.

The proof is not quite complete—we only know that $f$ is bounded on $[a, x]$ for every $x < b$, not necessarily that $f$ is bounded on $[a, b]$. However, only one small argument needs to be added.

There is a $\delta > 0$ such that $f$ is bounded on $\{x : b - \delta < x \leq b\}$. There is $x_0$ in $A$ such that $b - \delta < x_0 < b$. Thus $f$ is bounded on $[a, x_0]$ and also on $[x_0, b]$, so $f$ is bounded on $[a, b]$.

