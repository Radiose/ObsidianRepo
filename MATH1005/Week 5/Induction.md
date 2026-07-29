---
{}
---
Induction 
Induction is a method utilised in mathematical [[proof]]s. It is a form of [[Recursion]] used in mathematics, that is particularly useful for recursive data structures.


One of the most obvious examples is for [[Sequence]]s. Induction allows you to take the [[implicit definition of a sequence|implicit definition]] of a sequence, and then prove that an [[Explicit definition of a Sequence|explicit definition]] true.



This particular method is known as **strong mathematical induction**

let *P*(n) be a [[predicate]] with variable $n \in \mathbb{N}$
*proof of $\forall_{n}  \in \mathbb{N}\ P(n)$ by induction* 
1: Prove P(1) - the starting value 
3: let $n \in \mathbb{N}$ - an arbitrary positive integer 
Treat n as temporarily fixed and then:
3: **Assume** $p(1)\land p(2)\land p(3)\land\dots p(n)$. Induction utilises mechanisms that are used in [[Proving an implication]]
4: Prove P(n+1) to be true 

The idea with induction is to try to prove the $n+1$ case via assumption of the $n$ case (and possible $n-1,n-1\dots 1$ cases as well).  


### Weak induction 
Prove base case (p(0) or whatever starting value in [[Sequence]])

Prove inductive case:
**Assume p(n) holds** (inductive hypothesis)
use it to prove p(n+1) (most [[implicit definition of a sequence|implicit definition]]s have an easy of way of accommodating this)


This works because the basis of [[Proving an implication]] 

$P(1)$ is true 
$P(1) \implies P(2)$
We have proven that if p1 is true, then p2 is true. 
Also, if P(2) is true, then P(1) *must* be true, because it is a [[sufficient and necessary conditions|necessary condition]].
