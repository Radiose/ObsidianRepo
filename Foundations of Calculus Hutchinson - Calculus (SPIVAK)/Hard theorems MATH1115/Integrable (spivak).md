Integrable

# Motivation

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

## Theorem 1 
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

There is no good candidate for the [[Riemann sum]], so we say that this function is not integrable. 

# Definition
A function $f$ which is bounded on $[a, b]$ is **integrable** on $[a, b]$ if

$$
\sup\{L(f, P) : P \text{ a partition of } [a, b]\} = \inf\{U(f, P) : P \text{ a partition of } [a, b]\}.
$$

In this case, this common number is called the **integral** of $f$ on $[a, b]$ and is denoted by

$$
\int_a^b f.$$


# THEOREM 2
If $f$ is bounded on $[a, b]$, then $f$ is integrable on $[a, b]$ if and only if for every $\varepsilon > 0$ there is a partition $P$ of $[a, b]$ such that

$$
U(f, P) - L(f, P) < \varepsilon.
$$

**PROOF**  Suppose first that for every $\varepsilon > 0$ there is a partition $P$ with

$$
U(f, P) - L(f, P) < \varepsilon.
$$

Since

$$
\inf\{U(f, P')\} \le U(f, P),
$$
$$
\sup\{L(f, P')\} \ge L(f, P),
$$

it follows that

$$
\inf\{U(f, P')\} - \sup\{L(f, P')\} < \varepsilon.
$$

Since this is true for all $\varepsilon > 0$, it follows that

$$
\sup\{L(f, P')\} = \inf\{U(f, P')\};
$$

by definition, then, $f$ is integrable. The proof of the converse assertion is similar: If $f$ is integrable, then

$$
\sup\{L(f, P)\} = \inf\{U(f, P)\}.
$$

This means that for each $\varepsilon > 0$ there are partitions $P'$, $P''$ with

$$
U(f, P'') - L(f, P') < \varepsilon.
$$

Let $P$ be a partition which contains both $P'$ and $P''$. Then, according to the lemma,

$$
U(f, P) \le U(f, P''),
$$
$$
L(f, P) \ge L(f, P');
$$

consequently,

$$
U(f, P) - L(f, P) \le U(f, P'') - L(f, P') < \varepsilon. \quad \blacksquare
$$
Its clear that this theorem amounts to little more than restating the definition of integrable. 


## Example of this definition being useful 

Let $f$ be defined on $[0, 2]$ by

$$
f(x) = \begin{cases} 0, & x \ne 1 \\ 1, & x = 1. \end{cases}
$$
On first glance, this seems like its not integrable, but the definitions we have laid out demonstrate otherwise.

Suppose $P = \{t_0, \ldots, t_n\}$ is a partition of $[0, 2]$ with

$$
t_{j-1} < 1 < t_j
$$

(see Figure 8). Then

$$
m_i = M_i = 0 \quad \text{if} \quad i \ne j,
$$

but

$$
m_j = 0 \quad \text{and} \quad M_j = 1.
$$

Since

$$
L(f, P) = \sum_{i=1}^{j-1} m_i (t_i - t_{i-1}) + m_j (t_j - t_{j-1}) + \sum_{i=j+1}^{n} m_i (t_i - t_{i-1}),
$$

$$
U(f, P) = \sum_{i=1}^{j-1} M_i (t_i - t_{i-1}) + M_j (t_j - t_{j-1}) + \sum_{i=j+1}^{n} M_i (t_i - t_{i-1}),
$$

we have

$$
U(f, P) - L(f, P) = t_j - t_{j-1}.
$$
This is because $m_{j}$ and $M_{j}$ are the only points along the interval that are different, and because we have $M_{j}$ = 1, we can simplify it to just $t_{j}-t_{j-1}$

This certainly shows that $f$ is integrable: to obtain a partition $P$ with

$$
U(f, P) - L(f, P) < \varepsilon,
$$
Moreover, it is clear that

$$
L(f, P) \le 0 \le U(f, P) \quad \text{for all partitions } P.
$$

Since $f$ is integrable, there is only *one* number between all lower and upper sums, namely, the integral of $f$, so

$$\int_0^2 f = 0.$$

## Deriving the antiderivative of f(x) = x

Consider an interval $[0,b]$, with $b > 0$.

If $P = \{t_0, \ldots, t_n\}$ is a partition of $[0, b]$, then

$$
m_i = t_{i-1} \quad \text{and} \quad M_i = t_i
$$
(In other words, the left side of the subinterval is ALWAYS the smallest point in it ($m_{i}$), and the right side is always the largest ($M_{i}$))

and therefore

$$
L(f, P) = \sum_{i=1}^{n} t_{i-1}(t_i - t_{i-1})
$$
$$
= t_0(t_1 - t_0) + t_1(t_2 - t_1) + \cdots + t_{n-1}(t_n - t_{n-1}),
$$

$$
U(f, P) = \sum_{i=1}^{n} t_i (t_i - t_{i-1})
$$
$$
= t_1(t_1 - t_0) + t_2(t_2 - t_1) + \cdots + t_n(t_n - t_{n-1}).
$$

Neither of these formulas is particularly appealing, but both simplify considerably for partitions $P_n = \{t_0, \ldots, t_n\}$ into $n$ *equal* subintervals. In this case, the length $t_i - t_{i-1}$ of each subinterval is $b/n$, so

$$
t_0 = 0,
$$
$$
t_1 = \frac{b}{n},
$$
$$
t_2 = \frac{2b}{n}, \quad \text{etc};
$$
in general

$$
t_i = \frac{ib}{n}.
$$

Then

$$
L(f, P_n) = \sum_{i=1}^{n} t_{i-1}(t_i - t_{i-1})
$$
$$
= \sum_{i=1}^{n} \left\{ \frac{(i-1)b}{n} \right\} \cdot \frac{b}{n}
$$ (the left endpoint is $\frac{(i-1)b}{n}$)
$$
= \left[ \sum_{i=1}^{n} (i-1) \right] \frac{b^2}{n^2}
$$
$$
= \left( \sum_{j=0}^{n-1} j \right) \frac{b^2}{n^2}.
$$


Remembering the formula (the sum of integers from 1 to k)

$$
1 + \cdots + k = \frac{k(k+1)}{2},
$$

this can be written

$$
L(f, P_n) = \frac{(n-1)(n)}{2} \cdot \frac{b^2}{n^2}
$$
$$
= \frac{n-1}{n} \cdot \frac{b^2}{2}.
$$

Similarly,

$$
U(f, P_n) = \sum_{i=1}^{n} t_i (t_i - t_{i-1})
$$
$$
= \sum_{i=1}^{n} \frac{ib}{n} \cdot \frac{b}{n}
$$
$$
= \frac{n(n+1)}{2} \cdot \frac{b^2}{n^2}
$$
$$
= \frac{n+1}{n} \cdot \frac{b^2}{2}.
$$
The key bit here to notice here is if $n$ is very large, this approaches $\frac{b^2}{2}$. This makes it easy to show that $f$ is integrable. 

 Notice first that

$$
U(f, P_n) - L(f, P_n) = \frac{2}{n} \cdot \frac{b^2}{2}.
$$

This shows that there are partitions $P_n$ with $U(f, P_n) - L(f, P_n)$ as small as desired. By Theorem 2 the function $f$ is integrable. Moreover, $\int_0^b f$ may now be found with only a little work. It is clear, first of all, that

$$
L(f, P_n) \le \frac{b^2}{2} \le U(f, P_n) \quad \text{for all } n.
$$
This can be deduced simply with $\frac{n-1}{n}$ always being less than 1 etc. 

This inequality shows only that $b^2/2$ lies between certain special upper and lower sums, but we have just seen that $U(f, P_n) - L(f, P_n)$ can be made as small as desired, so there is *only one* number with this property. Since the integral certainly has this property, we can conclude that

$$
\int_0^b f = \frac{b^2}{2}.
$$


## Deriving the antiderivative of $x^2$

The function $f(x) = x^2$ presents even greater difficulties. In this case, if $P = \{t_0, \ldots, t_n\}$ is a partition of $[0, b]$, then

$$
m_i = f(t_{i-1}) = (t_{i-1})^2 \quad \text{and} \quad M_i = f(t_i) = t_i^2.
$$

Choosing, once again, a partition $P_n = \{t_0, \ldots, t_n\}$ into $n$ equal parts, so that

$$
t_i = \frac{i \cdot b}{n},
$$

the lower and upper sums become

$$
L(f, P_n) = \sum_{i=1}^{n} (t_{i-1})^2 \cdot (t_i - t_{i-1})
$$
$$
= \sum_{i=1}^{n} (i-1)^2 \frac{b^2}{n^2} \cdot \frac{b}{n}
$$
$$
= \frac{b^3}{n^3} \cdot \sum_{j=0}^{n-1} j^2,
$$

$$
U(f, P_n) = \sum_{i=1}^{n} t_i^2 \cdot (t_i - t_{i-1})
$$
$$
= \sum_{i=1}^{n} i^2 \frac{b^2}{n^2} \cdot \frac{b}{n}
$$
$$
= \frac{b^3}{n^3} \sum_{j=1}^{n} j^2.
$$

Recalling the formula

$$
1^2 + \cdots + k^2 = \frac{1}{6}k(k+1)(2k+1)
$$

these sums can be written as

$$
L(f, P_n) = \frac{b^3}{n^3} \cdot \frac{1}{6}(n-1)(n)(2n-1),
$$
$$
U(f, P_n) = \frac{b^3}{n^3} \cdot \frac{1}{6}(n+1)(2n+1).
$$

It is not too hard to show that

$$
L(f, P_n) \le \frac{b^3}{3} \le U(f, P_n),
$$

and that $U(f, P_n) - L(f, P_n)$ can be made as small as desired, by choosing $n$ sufficiently large. The same sort of reasoning as before then shows that

$$
\int_0^b f = \frac{b^3}{3}.
$$
## Theorem 3
If $f$ is [[continuous function|continuous]] on $[a,b]$, then $f$ is integrable on $[a,b]$

**PROOF**  Notice, first, that $f$ is bounded on $[a, b]$, because it is continuous on $[a, b]$. To prove that $f$ is integrable on $[a, b]$, we want to use Theorem 2, and show that for every $\varepsilon > 0$ there is a partition $P$ of $[a, b]$ such that

$$
U(f, P) - L(f, P) < \varepsilon.
$$

Now we know, by *Theorem 1* in [[uniform continuity]], that $f$ is uniformly continuous on $[a, b]$. So there is some $\delta > 0$ such that for all $x$ and $y$ in $[a, b]$,

$$
\text{if } |x - y| < \delta, \text{ then } |f(x) - f(y)| < \frac{\varepsilon}{2(b-a)}.
$$

The trick is simply to choose a partition $P = \{t_0, \ldots, t_n\}$ such that each $|t_i - t_{i-1}| < \delta$. Then for each $i$ we have

$$
|f(x) - f(y)| < \frac{\varepsilon}{2(b-a)} \quad \text{for all } x, y \text{ in } [t_{i-1}, t_i],
$$

and it follows easily that

$$
M_i - m_i \le \frac{\varepsilon}{2(b-a)} < \frac{\varepsilon}{b-a}.
$$

This is a smart trick, as we know that $f$ must take on the values $M_{i}$ and $m_{i}$ on the interval. 

Since this is true for all $i$, we then have

$$
U(f, P) - L(f, P) = \sum_{i=1}^{n} (M_i - m_i)(t_i - t_{i-1})
$$
$$
< \frac{\varepsilon}{b-a} \sum_{i=1}^{n} t_i - t_{i-1}
$$
$$
= \frac{\varepsilon}{b-a} \cdot b - a
$$ This can be observed earlier up the page
$$
= \varepsilon,
$$

which is what we wanted. $\blacksquare$

## Theorem 4
 Let $a < c < b$. If $f$ is integrable on $[a, b]$, then $f$ is integrable on $[a, c]$ and on $[c, b]$. Conversely, if $f$ is integrable on $[a, c]$ and on $[c, b]$, then $f$ is integrable on $[a, b]$. Finally, if $f$ is integrable on $[a, b]$, then

$$
\int_a^b f = \int_a^c f + \int_c^b f.
$$

**PROOF**  Suppose $f$ is integrable on $[a, b]$. If $\varepsilon > 0$, there is a partition $P = \{t_0, \ldots, t_n\}$ of $[a, b]$ such that

$$
U(f, P) - L(f, P) < \varepsilon.
$$

We might as well assume that $c = t_j$ for some $j$. (Otherwise, let $Q$ be the partition which contains $t_0, \ldots, t_n$ and $c$; then $Q$ contains $P$, so $U(f,Q) - L(f,Q) \le U(f,P) - L(f,P) < \varepsilon$  via the lemma. ) Either way, we can proceed with the proof. 


Now $P' = \{t_0, \ldots, t_j\}$ is a partition of $[a, c]$ and $P'' = \{t_j, \ldots, t_n\}$ is a partition of $[c, b]$ (Figure 12). Since

$$
L(f, P) = L(f, P') + L(f, P''),
$$
$$
U(f, P) = U(f, P') + U(f, P''),
$$

we have

$$
[U(f, P') - L(f, P')] + [U(f, P'') - L(f, P'')] = U(f, P) - L(f, P) < \varepsilon.
$$

Since each of the terms in brackets is nonnegative, each is less than $\varepsilon$. This shows that $f$ is integrable on $[a, c]$ and $[c, b]$. Note also that

$$
L(f, P') \le \int_a^c f \le U(f, P'),
$$
$$
L(f, P'') \le \int_c^b f \le U(f, P''),
$$

so that

$$
L(f, P) \le \int_a^c f + \int_c^b f \le U(f, P).
$$

Since this is true for any $P$, this proves that

$$
\int_a^c f + \int_c^b f = \int_a^b f.
$$

Now suppose that $f$ is integrable on $[a, c]$ and on $[c, b]$. If $\varepsilon > 0$, there is a partition $P'$ of $[a, c]$ and a partition $P''$ of $[c, b]$ such that

$$
U(f, P') - L(f, P') < \varepsilon/2,
$$
$$
U(f, P'') - L(f, P'') < \varepsilon/2.
$$

If $P$ is the partition of $[a, b]$ containing all the points of $P'$ and $P''$, then

$$
L(f, P) = L(f, P') + L(f, P''),
$$
$$
U(f, P) = U(f, P') + U(f, P'');
$$

consequently,

$$
U(f, P) - L(f, P) = [U(f, P') - L(f, P')] + [U(f, P'') - L(f, P'')] < \varepsilon. \quad \blacksquare$$



# THEOREM 5  
If $f$ and $g$ are integrable on $[a, b]$, then $f + g$ is integrable on $[a, b]$ and

$$
\int_a^b (f + g) = \int_a^b f + \int_a^b g.$$

**PROOF**  Let $P = \{t_0, \ldots, t_n\}$ be any partition of $[a, b]$. Let

$$
m_i = \inf\{(f+g)(x) : t_{i-1} \le x \le t_i\},$$
$$
m_i' = \inf\{f(x) : t_{i-1} \le x \le t_i\},$$
$$
m_i'' = \inf\{g(x) : t_{i-1} \le x \le t_i\},
$$

and define $M_i, M_i', M_i''$ similarly. It is not necessarily true that

$$
m_i = m_i' + m_i'',
$$

but it is true that

$$
m_i \ge m_i' + m_i''.
$$
or that the greatest lower bound of a sum of functions is greater than or equal to each functions greatest lower bound 

Similarly,

$$
M_i \le M_i' + M_i''.
$$

Therefore,

$$
L(f, P) + L(g, P) \le L(f+g, P)
$$

and

$$
U(f+g, P) \le U(f, P) + U(g, P).
$$

Thus,

$$
L(f, P) + L(g, P) \le L(f+g, P) \le U(f+g, P) \le U(f, P) + U(g, P).
$$

Since $f$ and $g$ are integrable, there are partitions $P'$, $P''$ with

$$
U(f, P') - L(f, P') < \varepsilon/2,
$$
$$
U(g, P'') - L(g, P'') < \varepsilon/2.
$$

If $P$ contains both $P'$ and $P''$, then

$$
U(f, P) + U(g, P) - [L(f, P) + L(g, P)] < \varepsilon,
$$via the lemma, 

and consequently

$$
U(f+g, P) - L(f+g, P) < \varepsilon.
$$

**This proves that $f+g$ is integrable on $[a, b]$.** 
Moreover,

$$
(1) \qquad L(f, P) + L(g, P) \le L(f+g, P) \le \int_a^b (f+g) \le U(f+g, P) \le U(f, P) + U(g, P);
$$

and also

$$
(2) \qquad L(f, P) + L(g, P) \le \int_a^b f + \int_a^b g \le U(f, P) + U(g, P).
$$

Since $U(f,P) - L(f,P)$ and $U(g,p) - L(g,P)$ can both be made as small as desired, it follows that

$$
U(f, P) + U(g, P) - [L(f, P) + L(g, P)]$$

can also be made as small as desired; it therefore follows from (1) and (2) that

$$\int_a^b (f+g) = \int_a^b f + \int_a^b g. \quad \blacksquare$$






# THEOREM 7

Suppose $f$ is integrable on $[a,b]$ and that

$$m \le f(x) \le M \quad \text{for all } x \text{ in } [a,b].$$

Then

$$m(b-a) \le \int_a^b f \le M(b-a).$$

**PROOF**  It is clear that

$$m(b-a) \le L(f,P) \quad \text{and} \quad U(f,P) \le M(b-a)$$

for every partition $P$. Since $\int_a^b f = \sup\{L(f,P)\} = \inf\{U(f,P)\}$, the desired inequality follows immediately. $\blacksquare$


# Theorem 8

**THEOREM 8**  If $f$ is integrable on $[a,b]$ and $F$ is defined on $[a,b]$ by

$$F(x) = \int_a^x f,$$

then $F$ is continuous on $[a,b]$.

**PROOF**  Suppose $c$ is in $[a,b]$. Since $f$ is integrable on $[a,b]$ it is, by definition, bounded on $[a,b]$; let $M$ be a number such that

$$|f(x)| \le M \quad \text{for all } x \text{ in } [a,b].$$

If $h > 0$, then (Figure 13)

$$F(c+h) - F(c) = \int_a^{c+h} f - \int_a^c f = \int_c^{c+h} f.$$

Since

$$-M \le f(x) \le M \quad \text{for all } x,$$

it follows from Theorem 7 that

$$-M \cdot h \le \int_c^{c+h} f \le Mh;$$

in other words,

$$\tag{1} -M \cdot h \le F(c+h) - F(c) \le M \cdot h.$$

If $h < 0$, a similar inequality can be derived: Note that

$$F(c+h) - F(c) = \int_c^{c+h} f = -\int_{c+h}^c f.$$

Applying Theorem 7 to the interval $[c+h, c]$, of length $-h$, we obtain

$$Mh \le \int_{c+h}^c f \le -Mh;$$

multiplying by $-1$, which reverses all the inequalities, we have

$$\tag{2} Mh \ge F(c+h) - F(c) \ge -Mh.$$

Inequalities (1) and (2) can be combined:

$$|F(c+h) - F(c)| \le M \cdot |h|.$$

Therefore, if $\varepsilon > 0$, we have

$$|F(c+h) - F(c)| < \varepsilon,$$

provided that $|h| < \varepsilon/M$. This proves that

$$\lim_{h \to 0} F(c+h) = F(c);$$

in other words $F$ is continuous at $c$. $\blacksquare$

The goal of this proof above was to proof that $F$ is continuous at any arbitrary point $c$. We did this via an [[The formal definition of a limit|epsilon delta proof]] $|h-0|<\delta \implies |F(c+h)-F(c)|<\epsilon$ (note that we can define $F(c+h) = g(h)$ for simplicity, so $|g(h)-L| <\epsilon$ ).


