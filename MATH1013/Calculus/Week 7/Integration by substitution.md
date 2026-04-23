---
aliases:
  - U-substitution
---
U substitution

This is a technique used when finding the [[Indefinite integral|antiderivative]] of a function. It is the most unique method discussed thus far in calculus.
This is essentially the reverse [[Chain rule]].


This is used to make it easier to tell that a function is of the form $F'(G(x))G'(x)$. 
It is easy to tell when a function is of the [[composition of Functions]], but exactly how those pieces fit together is much harder. THIS, is where U substitution works. 

### The substitution rule
If *u = g(x)* is a differentiable function whos range is an interval *I* and *f* is [[continuous function|continuous]] on I, then 
$\int f(g(x))g'(x)\ dx = \int f(u)\ du$

In fact, if $u = g(x)$, then $\frac{du}{dx}=g'(x)$ so $du = g'(x)dx$
That is, it is permissible to work with dx and du after integral signs as if they are differentials.
(A bit of weird algebraic manipulation)



#### Example 
$\int 2x \sqrt{ 1+x^2 }$
u = $1+x^2$
du = $2x \ dx$
$dx = \frac{1}{2x}du$
thus 
$\int 2x \sqrt{ u } \frac{1}{2x}du$
$\iff \int \sqrt{ u} \ du$


