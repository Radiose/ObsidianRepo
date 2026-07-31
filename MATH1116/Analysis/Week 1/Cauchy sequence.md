---
aliases:
  - cauchy
---
# Theorem
A [[Sequence]] [[Convergence of a sequence|converge]]s if and only if it is Cauchy. I.E
$\forall \epsilon>0 \ \ \ \exists n\ \ \ \forall n,m>N\ \ |x_{n}-x_{m}|<\epsilon$

This theorem is treated as an axiom in construction of the [[real number|reals]]. 


Axiom: Let $(x_{n})_{n \in \mathbb{N}}\in \mathbb{R}^\mathbb{N}$ be non decreasing and bounded, then $x_{n}$ [[Convergence of a sequence|converge]]s. 

Proof:
$[\implies]$ Assume $(x_{n})_{n \in \mathbb{N}}$ converges, that is $\forall\epsilon>0 \ \ \exists N \in \mathbb{N}\ \ \forall n>N\ \ |x_{n}-L|<\epsilon$

Then $\exists N \in \mathbb{N}\ \ \forall n\geq N\ \ |x_{n}-L|< \frac{\epsilon}{2}$, therefore $\forall n,m \geq N\ \ |x_{n}-x_{m}|\leq|x_{n}-l|+|l-x_{m}|<\epsilon$
$[\impliedby]$ (the challenge with this direction is that its hard to prove that they converge to some actual point rather than just being together forever).

Assume $(x_{n})_{n \in \mathbb{N}}$ is Cauchy. 

Define $(y_{n})_{n \in \mathbb{N}}\in \mathbb{R}^\mathbb{N}$ by $y_{n}=inf_{\ k\geq n}\ x_{k}$, that is, the greatest lower bound of all $x_{k}$ when $k \geq n$.
Remark: $y_{n+1}\geq y_{n}\ \ \ \ \forall n \in \mathbb{N}$ - either the greatest lower bound is the same, or its been 
