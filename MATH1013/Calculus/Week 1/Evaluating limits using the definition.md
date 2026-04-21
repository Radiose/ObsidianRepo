Evaluating limits using the definition
 Limit of a constant
 Prove that $\lim_{ k \to a }(k)=k$, where k is a constant
 step 1: the domain of f(x) is $\mathbb{R}$, so f(x) is defined around a
 $N(a,\delta)$ = $(a-\delta,a)\cup(a,a+\delta)\subset \mathbb{R}$ = domain(f) for all $\delta>0$

This step basically just shows that there exists a neighbourhood around a where every point of it is in the domain of f

step 2:
let $\epsilon \in (0,\infty)$. We can choose $\delta_{\epsilon}$ to be any positive value since
$0<|x-a|<\delta_{\epsilon} \implies |f(x)-l_{a}|=|k-k|=0<\epsilon$

Recall that the formal limit definition states that $\forall_{\epsilon}$ where $\epsilon>0$. therefore, using logic this statement is true regardless of the outcome of the left hand side of the equation 


Evaluating the limit of the identity function
identity function f(x) = x

step 1: the domain of f(x) is $\mathbb{R}$, so f(x) is defined around a
 $N(a,\delta)$ = $(a-\delta,a)\cup(a,a+\delta)\subset \mathbb{R}$ = domain(f) for all $\delta>0$

2: let $\epsilon \in (0,\infty).$ We can choose $\delta_{\epsilon}$ to be equal to $\epsilon$.
since $0<|x-a|<\delta = \epsilon \implies |f(x)-L_{a}|=|x-a|<\epsilon$

because |x-a| < $\delta$, $|f(x)-L_{a}|<\epsilon$
This is [[proof]]. This is just saying if you restrict the function to $\epsilon$, there must always be a $\delta$ that is greater than x-a. 


Evaluating the limit f(x) = (x+1) = 2
$L_{1}$ = 2
step 1: the domain of f(x) is $\mathbb{R}$, so f(x) is defined around a
 $N(a,\delta)$ = $(a-\delta,a)\cup(a,a+\delta)\subset \mathbb{R}$ = domain(f) for all $\delta>0$

2:
let $\epsilon \in (0,\infty).$ We can choose $\delta_{\epsilon}$ to be equal to $\epsilon$.
$0<|x-1|<\delta_{\epsilon}=\epsilon\implies|f(x)-L_{1}|=|(x+1)-2|=|x-1|<\epsilon$

evaluating $\lim_{ x \to 2 }(2x+3)=7$
recall that $\lim_{ x \to a }f(x)=L_{a}$
step 1: the domain of f(x) is $\mathbb{R}$, so f(x) is defined around a
 $N(a,\delta)$ = $(a-\delta,a)\cup(a,a+\delta)\subset \mathbb{R}$ = domain(f) for all $\delta>0$

step 2:
$\delta_{\epsilon} = \frac{\epsilon}{2}$
$0<|x-2|<\delta_{\epsilon}=\frac{\epsilon}{2}\implies |f(x)-L_{2}| = |(2x+3)-7|=|2x-4|=|2x-4|=2|x-2|<2\left( \frac{\epsilon}{2} \right)=\epsilon$