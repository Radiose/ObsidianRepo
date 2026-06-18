The real numbers are an essential part of calculus. Simply put, real numbers are numbers that can be expressed as decimals. 
EG:$5 = 5.000\dots$
$\frac{1}{3} = 0.33333\dots$


Ancient greeks through of real numbers as lengths of lines, and they knew that if $x$ is the length of the hypotenuse of the following right angled triangle, then its square must satisfy $x^2 = 1^2+1^2 = \sqrt{ 2 }$ .
![[Pasted image 20260618141317.png]]
Greeks thought of numbers as ratios of integers, so when they uncovered the following [[theorem]], they were quite upset.

Theorem: $\sqrt{ 2 }$ is not rational
Proof: we argue by contradiction. We assume $\sqrt{ 2 }=\frac{m}{n}\text{   where   } m,n \in \mathbb{Z}$

Multiplying numerator and denominator by -1 if necessary, we can take m, n to be positive. By cancelling if necessary, we can reduce to the situation where m and n have no common factors. Squaring both sides of the equation, we have 
$2 = \frac{m^2}{n^2}$ and hence $m^2=2n^2$
It follows that m is even, since the square of an odd number is odd. 
More precisely, if m was odd, we could write m = 2x + 1 for some integer x, but then $m^2$ = $(2x+1)(2x+1) = 4x^2+4x+1 = 2(2x^2+2x)+1$ which is odd, not even. 

Since m is even, we can write $m = 2p$ for some integer p 
and hence 
$m^2 = 4p^2$
substituting this into $m^2 = 2n^2$ gives 
$4p^2 = 2n^2$
and hence $2p^2 = n^2$.
since, this leads to the conclusion that n is even (via similar reasoning to m), then n and m have both the common factor 2, which contradicts the fact they have no common factors. 
This contradiction implies that our original assumption was wrong, and that $\sqrt{ 2 }$ is not rational. 



## Properties of the reals 
### Algebraic properties
The basics of these are that reals can be added, subtracted, multiplied and divided (not by zero) and that these operations are closed, they create more real numbers. 
### Order properties 
The order properties of the reals relates to the order of the number line. If $a,b \in \mathbb{R}$, $a < b \implies$ a is less than b. The order properties are summarised in the following rules
![[Inequality]]
### Completeness
If A is any set of real numbers having at least one number in it, and if there exists a real number y s.t $\forall x\in A\ \ \ \ x \le y$, (we denote y the *upper bound*) then there exists a smallest such number, called the *least upper bound*, or *supremum* of A.
