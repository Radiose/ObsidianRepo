---
aliases:
  - algebraic axiom
  - order axiom
---
The [[Real number]] system consists of the real numbers, along with the two operations addition(denoted $+$) and multiplication (denoted $\times$) and the less than [[relation]] (denoted by <). One also singles out two particular numbers being 0 and 1. 

If $a$ and $b$ are real numbers, then so are $a+b$ and $a \times b$. 
We usually write $ab$ for $a \times b$
For any real numbers, the [[Statement]] $a <b$  is either true of false. 

## Algebraic axioms
1: $a+b = b+a$ (commutative axiom for addition)
2: $(a+b)+c = a+(b+c)$ (associative axiom for addition)
3: $a+0 = 0+a = a$ (additive identity axiom)
4: there is a real number $-a$ such that $a + (-a) = (-a)+a=0$ (additive inverse axiom)
5:$a \times b =b \times a$ (commutative axiom for multiplication)
6: $(a \times b) \times c = a \times (b \times c)$ (associative axiom for multiplication)
7: $a \times 1 = 1 \times a = a$ and $0 \not=1$(multiplicative identity axiom) 
8: if $a \not=0$ there is a real number $a^{-1}$ such that $a \times a^{-1} = a^{-1}\times a = 1$ (multiplicative inverse axiom)
9: $(a + b)\times c = a \times b + a \times c$ (distributive axiom)


## Order axioms 
For all real number $a,\ b$ and $c$
10: exactly one of the following holds:
	$a<b$ or $a = b$ or $a > b$ (trichotomy axiom)
11: if $a < b$ and $b <c$, then $a < c$ (transitivity axiom)
12: if $a < b$ then $a + c < b  +c$ (addition and order axiom)
13: if $a < b$ and $0 < c$, then $a \times c  < b \times c$ (multiplication and order axiom)



Some notes:
We take the symbol $=$ to mean "denotes the same thing as", or equivalently "represents the same real number as". We take $=$ to be a logical notation and thus dont need any axioms. 

We are not using subtraction in axiom 4. We are merely stating that a real number with these properties exists. 

Parts of axioms are redundant. For example, from axiom 1, a + 0=a implies 0+a = a

## Defining subtraction and division 

We define the operation $a-b$ to be $a+(-b)$, and we define $a \div b$ to be $a \times b^{-1}$. Division by zero is never defined. 


## Cancellation theorem 
If $a, b, c$ are real numbers, and $a + c = b + c$, then $a = b$. Similarly, if $c + a = c + b \text{, then } a = b$.

proof: 
Assume $a+c = b+c$
Since $a+c$ and $b+c$ denote the same real number, we obtain the same result if we add -c to it. i.e
$(a+c) + (-c)  = (b+c)+ (-c)$
Via the commutative axiom applied twice (to each side of the equation) 
$a + (c + -c) = b + (c + - c)$
Now via axiom 2 applied twice (to each side of the equation) 
$a +0 = b+0$
Now from axiom 4 applied twice (to each side of the equation)
$a=b$
thus, if $a+c = b+c$, then this implies that $a = b$


## Characterisation of *0* and *-a*
Is there more than one real number such that $a+x = x+a = a$?
Via axioms 2 and 3, we have that $a+0 = x+a = a$
Via the cancellation theorem, 0 = x. Thus, there is only the number 0.

A similar thing can be done to prove the uniqueness of $-a$
Suppose $a+x=0$, we know from the fourth axiom that $a+x = (-a)+a$
Thus, via cancellation theorem, $x = -a$

