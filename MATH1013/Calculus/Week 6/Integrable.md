Integrable
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
Let $P_{1}$ and $P_{2}$ be partitions of $[a,b]$ and let $f$ be a function that is bounded on $[a,b]$. Then, $$L(f, P_{1}) \leq U(f,P_{2})$$
Proof:
There is a partition $P$ which contains both $P_{1}$ and $P_{2}$. According to the lemma, $L(f,P_{1})\leq L(f,P)\leq U(f,P) \leq U(f,P_{2}) \blacksquare$



# Relating this theorem to Integration  

Using theorem 1 in [[Riemann sum]], it follows that any upper sum $U(f,P')$ is an upper bound for the *set* of all *lower* *bounds* $L(f,P)$. Any upper sum $U(f,P')$ is greater than or equal to the [[Completeness axiom|least upper bound]] of all lower sums : $sup \{ L(f,P):P \text{ a partition of }[a,b] \} \leq U(f,P')$
for all $P$. 
This in turn means that $sup \{ L(f,P) \}$ is a lower bound for the set of all upper sums of $f$. 

Consequently, $sup \{ L(f,P)\leq inf(U(f,P)) \}$. That is, the **least upper bound** of the **lower sums** is less than or equal to the **greatest lower bound** of the **upper sums**.

It is clear that both of these numbers are between the lower sum and upper sum of $f$ for *all* partitions:

$$
L(f, P') \le \sup\{L(f, P)\} \le U(f, P'),
$$
$$
L(f, P') \le \inf\{U(f, P)\} \le U(f, P'),
$$

for all partitions $P'$.

It may well happen that

$$
\sup\{L(f, P)\} = \inf\{U(f, P)\};
$$
And in this case, this is the only number that is between the lower and upper sum of $f$ *for all* partitions. This number is an ideal candidate for the area of $R(f,a,b)$. 

On the other hand, if$$
\sup\{L(f, P)\} < \inf\{U(f, P)\};
$$then every number $x$ between $\sup\{L(f, P)\}$ and $\inf\{U(f, P)\}$ will satisfy

$$
L(f, P') \le x \le U(f, P')
$$

for all partitions $P'$.

We show some examples for this

Suppose first that $f(x) = c$ for all $x$ in $[a, b]$ (Figure 6). If $P = \{t_0, \ldots, t_n\}$ is any partition of $[a, b]$, then $$ m_i = M_i = c, $$ so $$ L(f, P) = \sum_{i=1}^{n} c(t_i - t_{i-1}) = c(b - a), $$ $$ U(f, P) = \sum_{i=1}^{n} c(t_i - t_{i-1}) = c(b - a). $$
In this case, all lower and upper sums are equal, and thus 
$$
\sup\{L(f, P)\} = \inf\{U(f, P)\}=c(b-a);
$$

Now consider the function defined by $0$ if $x$ is irrational, and $1$ if $x$ is rational. 

If $P = \{t_0, \ldots, t_n\}$ is any partition, then

$$
m_i = 0, \quad \text{since there is an irrational number in } [t_{i-1}, t_i],
$$

and

$$
M_i = 1, \quad \text{since there is a rational number in } [t_{i-1}, t_i].
$$

Therefore,

$$
L(f, P) = \sum_{i=1}^{n} 0 \cdot (t_i - t_{i-1}) = 0,
$$

$$
U(f, P) = \sum_{i=1}^{n} 1 \cdot (t_i - t_{i-1}) = b - a.
$$
In this case, we see that $\sup\{L(f, P)\} \not = \inf\{U(f, P)\}$