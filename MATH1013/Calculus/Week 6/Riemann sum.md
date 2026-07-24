---
{}
---
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



# Analysis (formal definition)
Suppose $f$ is bounded on $[a,b]$ and $P =\{ t_{0},\dots,t_{n} \}$ is a [[partition]] of $[a,b]$. Let $m_{i} = inf\{ f(x): t_{i-1} \leq x \leq t_{i} \}$ 
and $M_{i}=sup \{ f(x): t_{i-1} \leq x \leq t_{i} \}$

The lower sum of $f$ for $P$, denoted by $L(f,P) = \sum_{i=1}^n m_{i}(t_{i}-t_{i-1})$
The upper sum of $f$ for $P$, denoted by $U(f,P)=\sum_{i-1}^n M_{i}(t_{i}-t_{i-1})$.
This is the formal way of denoting upper and lower sums, where we take the largest and the smallest element of the codomain of $f$ (the shortest and tallest $y$ value).

A result that is not quite obvious but is true is that for any two partitions $P_{1},P_{2}$ of an interval $[a,b]$, we have that $L(f,P_{1}) \leq U(f,P_{2})$
This is because $L(f,P_{1})$ should be less than the actual area, and $U(f,P_{2})$ should be greater. 

# Lemma
Let $Q$ and $P$ be both partitions of the same interval
If $Q$ contains $P$ (that is, all elements of $P$ are also in $Q$), 
then $L(f,P) \leq L(f,Q)$
and $U(f,P)\geq U(f,Q)$
![[Pasted image 20260724164229.png]]
Here we have $P$ representing the points in black, and $Q$ representing the points in black and grey. 

Proof 

Let $$ m' = \inf\{f(x) : t_{k-1} \le x \le u\}, $$ $$ m'' = \inf\{f(x) : u \le x \le t_k\}. $$ Then $$ L(f, P) = \sum_{i=1}^{n} m_i (t_i - t_{i-1}), $$ $$ L(f, Q) = \sum_{i=1}^{k-1} m_i (t_i - t_{i-1}) + m'(u - t_{k-1}) + m''(t_k - u) + \sum_{i=k+1}^{n} m_i (t_i - t_{i-1}). $$ That is, the sum of everything up to the point, the sum of everything after the point, and the two rectangles attached to the points left and right. 
 

To prove that $L(f, P) \le L(f, Q)$ it therefore suffices to show that $$ m_k (t_k - t_{k-1}) \le m'(u - t_{k-1}) + m''(t_k - u). $$
The trick to this proof is that the set $\{f(x) : t_{k-1} \le x \le t_{k}\}$ contains all numbers in $\{f(x) : t_{k-1} \le x \le u\}$, and possibly some smaller ones, so the greatest lower bound of the first set is less than or equal to that of the second set. 
$m_{k}\leq m'$ and similarly, $m_{k}\leq m''$, therefore $$ m_k (t_k - t_{k-1}) = m_k (u - t_{k-1}) + m_k (t_k - u) \le m'(u - t_{k-1}) + m''(t_k - u). $$
Now, we can simply create a [[Sequence]] of these partitions that will become $Q$. That is, we create a sequence of partitions that are one point larger than the previous, and in turn we will obtain $Q$ after some amount of steps. 
The sequence is shown below
$$ P = P_1, P_2, \ldots, P_\alpha = Q $$ such that $P_{j+1}$ contains just one more point than $P_j$. Then $$ L(f, P) = L(f, P_1) \le L(f, P_2) \le \cdots \le L(f, P_\alpha) = L(f, Q), $$ and $$ U(f, P) = U(f, P_1) \ge U(f, P_2) \ge \cdots \ge U(f, P_\alpha) = U(f, Q). \quad \blacksquare $$ The theorem we wish to prove is a simple consequence of this lemma.

Theorem 1 
Let