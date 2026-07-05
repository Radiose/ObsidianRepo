Theorems for [[continuous function|continuous]]ness

## Simple theorems to make it easier 

Some important theorems that are part of proofs for continuity are the following 
1: If $f,\ g$ are continuous at $a$, then 
	- $f+g$ is continuous at $a$
	- $f \cdot g$ is continuous at $a$
Moreover, if $g(a) \not=0$, then $\frac{1}{g}$ is continuous at $a$

This theorem is extremely useful for proving compositions of functions are continuous. Because we know that $f(x) = c$, $g(x) = x$ and $h(x) = x^2$ are all continuous at any $a$, then a function $f(x) = \frac{ b_{n}x^n + b_{n-1}x^{n-1}\dots b_{0}}{c_{m}x^m + c_{m-1}x^{m-1}\dots c_{0}}$ is continuous at any $a$.


2: If $g$ is continuous at $a$ and $f$ is continuous at $g(a)$, then $f \circ g$ is continuous at $a$. 

(Notice that $f$ is required to be continuous at $g(a)$, not at $a$, which follows from the definition of function [[composition of Functions|composition]]).

We utilise a simple proof 
Let  $g$ be continuous at $a$, let $f$ be continuous at $g(a)$
$|x-a| < \delta \implies$ $|(f \circ g)(x) - (f \circ g)(a)| < \epsilon$

Because $f$ is continuous at $g(a)$, $\exists\  \delta' >0 \ \ \forall y$ 
1: $|y-g(a)|<\delta' \implies|f(y)-f(g(a))|<\epsilon$
In particular, this means that 
2: $|g(x)-g(a)|<\delta' \implies |f(g(x))-f(g(a))|<\epsilon$

Now, because $g$ is continuous at $a$, we can take $\delta'$ to be the $\epsilon$ involved for it. 
That is, 
3: $|x-a|<\delta \implies |g(x)-g(a)|<\delta'$

Note how RHS of 3 and LHS of 2 are identical. 

combining 2 and 3, we get 
$\forall x$   $|x-a|<\delta \implies |f(g(x))-f(g(a))|<\epsilon \ \blacksquare$ 
