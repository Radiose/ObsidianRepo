---
{}
---
So the formal definition of a [[limits|limit]] is
for a function f(x) and real number a and $l_{a}$, we write $\lim_{ x \to a }f(x)=L_{a}$, and we say that the limit of f(x) as x approaches a is $l_a$, or f(x) approaches $L_{a}$ as x approaches a, when:
1: there exist $\delta \in (0,\infty)$ such that N(a,$\delta$) = $(a-\delta,a)\cup (a,a+\delta)$ is a subset of the domain of f(x): $N(a,\delta) \subset Domain (f)$; and
2: for every $\epsilon \in N(a,\delta_{\epsilon})$, there exists $\delta_{\epsilon} \in (0,\infty)$ such that

$x \in N(a,\delta_{\epsilon})$, that is |x-a|<$\delta_{\epsilon}$ and  $x \not= a \implies |f(x)-L_{a}|<\epsilon$

if no such $L_a$ exists, we say that $\lim_{ n \to \infty }f(x)$ does not exist 

This is basically saying that for every epsilon difference, there must also be a delta difference.



## HOW TO GO ABOUT PROVING 
The essence of an $\epsilon-\delta$ problem is to convert the $f(x)-l$ expression into a factorised $|x-a|\times|something|$ . 

From here, we create a bound on $|x-a|$ that upon rearranging, gives us $x < z$.
From here, we use the property of $x < z$ to do a couple of options: 
1: use the triangle inequality on the $|something|$ and substitute in what $x$ is less than ($x < z$) to get another value $|something|$ is less than. 

Basically, we want to use the property that $|x-a|$ is less than something to find out what $|something|$ is less than. From here, we say $|x-a|\times|something|< |x-a| \times\text{something that |something| is less than}<\epsilon$. then rearrange to get $|x-a|< \frac{\epsilon}{\text{something that |something| is less than}}$
Thus, delta is $min(z, \frac{\epsilon}{\text{something that |something is less than|}})$

The most important part is understanding 
$$|x-a|\times|something|< |x-a| \times\text{something that |something| is less than}<
\epsilon$$
