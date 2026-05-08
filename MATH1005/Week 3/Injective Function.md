---
aliases:
  - injective
  - one to one
---
Injective [[function]]s
Let $f: A \to B$ be a function. We say that f is one-to-one, or that f is injective when 
$\forall a_{1},a_{2} \in A(a_{1} \not=a_{2}) \implies f(a_{1})\not=f(a_{2})$
For every input, there exists a unique output **and for every output, there exists a unique input**. So it passes the horizontal line test. 

Proving if f :$\mathbb{N} \to \mathbb{N}$ defined by f(a) = $a^2$ is injective 
Yes. to show this we show that 

$\forall a_{1},a_{2} \in A(a_{1} =a_{2}) \implies f(a_{1})=f(a_{2})$



When constructing a [[proof]] around whether a function is injective, it is easier to prove the contrapositive.


## monotone functions 
A [[function]] can be proven to be injective on the interval (a,b) if $\forall x \in (a,b)$, $f$ is differentiable, and $f'(x)>0$. Similarly, by the same logic, $f'(x)<0$ for all x will prove f is injective. 

Some tools that will help for this is the discriminant, and the fact that even powers are always positive. If the discriminant has no solutions, then it never crosses the x axis. Thus, if the derivatives discriminant never crosses, it must always be positive or negative


