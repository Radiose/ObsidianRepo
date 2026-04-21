Riemann sum 
For any real numbers *a,b* with $a<b$ and any positive integer n, a [[partition]] of \[a,b] (into n sub intervals) is an (n+1) tuple of real numbers $P=(x_{0},x_{1}\dots x_{n})$ such that $a = x_{0}<x_{1}<\dots<x_{n-1}<x_{n}=b$

Given a [[partition]] p, 
- For each $i \in \{ 1,2,\dots ,n \}$, we write $\Delta x_{i}$ for the quantity $x_{i}-x_{i-1}$
- We write $||P||$ for $max\{ \Delta_{1}, \Delta_{2}\dots \Delta_{n} \}$, or known as the **norm** of the partition 
- A choice of sample points associated to P is an n-tuple of points S = $\{ x_{1}^* , x_{2}^*,\dots x_{n}^* \}$ such that $\forall _i \in \{ 1,2\dots,n \}\ \  \exists x_{i}^*\in [x_{i-1},x_{i}]$ 


Given a partition P and an associated choice of sample points S,
The quantity $\sum_{i=1}^n f(x_{i}^*)\Delta x_{i}$ is called the **Riemann sum** of f on \[a,b] associated to P and S and is denoted $R(f,P,S)$

![[Pasted image 20260331173245.png]]
Looking at this, you can see the height is the sample point, and the width is the $\Delta x_{i}$

A [[Riemann sum]] is a good method for approximating the area under a curve. It can be deducted then, that as $||P||$ gets smaller, the area approximation gets more accurate. 
