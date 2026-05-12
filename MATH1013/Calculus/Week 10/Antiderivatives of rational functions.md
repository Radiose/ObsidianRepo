Antiderivatives of rational [[function]]s

Some examples of rational functions 
$\int \frac{6}{(x+10)^3}dx$ - this can be done with u substitution 

Another one 
$\int \frac{x}{x^2+2x+10}dx$ - use u substitution, except represent x as a multiple of derivative of the denominator. 

### Terminology
$f$ is a rational function if $f(x) = \frac{p(x)}{q(x)}$ where p and q are polynomials 
$f$ is proper if the degree of the denominator is greater than the degree of the numerator. 
$f$ is improper if he numerator is larger, but this is ok because we can just divide p by q.
The rule $\frac{7}{3}=2+\frac{1}{3}$ is the same idea 
$\frac{x^3+2x^2+1}{x^2+1}$ - use polynomial long division - remainder is the numerator, we put the dividend outside and sum it with the numerator divided by the original denominator

A quadratic polynomial is **irreducible** if it has no real linear factors. Equivalently, quadratic $ax^2+bx+c$ is irreducible if the **discriminant** is negative, so there are no real roots. 

It can be shown that **every** *proper* *rational* function can be written as such 
$\frac{A}{(x+a)^k}$ and $\frac{A}{(x^2+bx+c)^k}$
 where the quadratic on the bottom right is irreducible.



There are four cases we shall deal with for decomposing a rational function $\frac{p(x)}{q(x)}$

   
## q(x) is a product of linear factors, none of which are repeated
This looks like 
$\frac{x-3}{(x-1)(x-2)}$ = $\frac{A}{(x-1)}+\frac{B}{x-2}$

To solve, create a large fraction containing both 
$A(x-2)+B(x-1) = (x-3)$
Find x's that zero out a factor, EG x = 2 
$A(0)+B(2-1)=2-3$
$\therefore B\times 1=-1$
$\implies B = -1$
and $x = 1$
$A(1-2)+B(0)=(1-3)$
$-A = -2$
$A = 2$
## q(x) is a product of linear factors, some of which are repeated

This looks like 
$\frac{x^2+2}{(x+4)^3}$ or $\frac{x^2+2}{(x-2)^2(x-1)}$
these get turned into 
$\frac{A}{(x+4)} + \frac{B}{(x+4)^2}+\frac{C}{(x+4)^3}$
and 
$\frac{A}{(x-1)} + \frac{B}{(x-2)} + \frac{C}{(x-2)^2}$

You can solve this in a similar way. Youd end up with 
$A(x-2)^2 +B(x-1)(x-2)+C(x-1) = x^2 +2$

## q(x) contains irreducible quadratic factors, none of which are repeated
These look like $\frac{x^2+x}{(x-1)(x^2+9)} \to \frac{A}{x-1}+ \frac{Bx+C}{x^2+9}$
and $\frac{x^3-2x+4}{(x^2+5)(x^2+x+1)} \to \frac{Ax+B}{x^2+5} + \frac{Cx + D}{x^2+x+1}$

## q(x) contains irreducible quadratic factors, none of which are repeated
Same as for linear factors 
![[Pasted image 20260513081228.png]]
