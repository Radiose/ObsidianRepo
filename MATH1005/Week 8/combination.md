---
aliases:
  - choose
---
combination

This is used when order *doesn't* matter. IE, when you are treating [[subset]]s of a set by definition. 

There are $C(n,r) = \begin{pmatrix} n  \\ r\end{pmatrix} = \frac{P(n,r)}{r!} = \frac{n!}{r!(n-r)!}$ ways to choose a set of r out of n. This makes sense logically. What we are doing is getting the [[permutation]], and then dividing it by the amount of distinct ways that a set of r can be arranged with the same elements. IE, we are removing the sets of r that are in different orders but have the same elements.


## Set definition 
$\begin{pmatrix}n  \\ r\end{pmatrix}$ can be thought of as the no of sets of size r from n 

![[Pasted image 20260429120359.png]]
