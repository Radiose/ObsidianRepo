This technique is one of the essential analysis tools. It is the discrete analogue to [[Integration by parts]].
## Lemma
Let $(a_j)_{j\in\mathbb{N}}, (b_j)_{j\in\mathbb{N}} \in \mathbb{R}^{\mathbb{N}}$, and $n \in \mathbb{N}$. Then

$$
\sum_{k=0}^{n} a_k(b_{k+1} - b_k) = -\sum_{k=1}^{n} (a_k - a_{k-1})b_k + a_n b_{n+1} - a_0 b_0.
$$
### Proof
let $n \in \mathbb{N}^*$
$$
\begin{aligned}
\sum_{k=0}^{n} a_k(b_{k+1} - b_k) &= \sum_{k=0}^{n} a_k b_{k+1} - \sum_{k=0}^{n} a_k b_k \\
&= \sum_{k=1}^{n+1} a_{k-1} b_k - \sum_{k=1}^{n} a_k b_k \\
&= \sum_{k=1}^{n} (a_{k-1} - a_k) b_k + a_n b_{n+1} - a_0 b_0.
\end{aligned}
$$
This is just peeling of series. 

# Corollary 
Let $(a_j)_{j\in\mathbb{N}}, (b_j)_{j\in\mathbb{N}} \in \mathbb{R}^{\mathbb{N}}$ and $n \in \mathbb{N}$. Then

$$
\sum_{k=0}^{n} a_k b_{k+1} = -\sum_{k=1}^{n} (a_k - a_{k-1}) \left(\sum_{j=0}^{k} b_j\right) + a_n \left(\sum_{j=0}^{n+1} b_j\right) - a_0 b_0.
$$
### Proof
Just apply summation by parts with $b_{k}=\sum_{j=0}^n b_{j}$.


# Applications

# Theorem 1 
> [!theorem]
> Let $(a_j)_{j \in \mathbb{N}}, (b_j)_{j \in \mathbb{N}} \in \mathbb{R}^{\mathbb{N}}$ be such that
> (i) $\lim_{n \to +\infty} a_n = 0$
> (ii) $\sum_{n=0}^{\infty} |a_{n+1} - a_n|$ converges
> (iii) $\exists M > 0, \forall n \in \mathbb{N}, \left| \sum_{j=0}^{n} b_j \right| \le M$
>
> then $\sum_{k=0}^{\infty} a_k b_{k+1}$ converges.

**Proof.** We have $\left| (a_k - a_{k+1}) \sum_{j=0}^{k} b_j \right| \le M |a_k - a_{k+1}|, \; \forall k \ge 0$. Therefore

$$
\sum_{k=1}^{\infty} (a_k - a_{k-1}) \left( \sum_{j=0}^{k} b_j \right) \text{ converges.}
$$

Also $\left| a_n \sum_{j=0}^{n+1} b_j \right| \le M |a_n|, \; \forall n \in \mathbb{N}$. Therefore $\lim_{n \to +\infty} a_n \left( \sum_{j=0}^{n+1} b_j \right) = 0$, and hence

$$
\left( -\sum_{k=0}^{n} (a_k - a_{k-1}) \sum_{j=0}^{k} b_j + a_n \sum_{j=0}^{n+1} b_j - a_0 b_0 \right)_{n \in \mathbb{N}} \text{ converges.}
$$

The series $\sum_{k=0}^{\infty} a_k b_{k+1}$ converges by the above corollary. $\blacksquare$



# Corollary
Let $(a_{j})j \in \mathbb{N} \in \mathbb{R}^\mathbb{N}$ be such that

1: $a_{j}\geq {0} \ \ \ \forall j \in \mathbb{N}$

2: $a_{j+1}\leq a_{j} \ \ \ \ \forall j \in \mathbb{N}$

3: $\lim_{ j \to \infty }a_{j}=0$

Then $\sum_{j=0}^\infty(-1)^ja_{j}$ converges. 





# Examples

Prove $\sum_{n=0}^\infty \frac{(-1)^n}{\ln(n+2)}$ converges:
we use theorem 1 above.
Let $a_{n} = \frac{1}{\ln(n+2)}$
Let $b_{n}=(-1)^{n-1}$

$\lim_{ n \to \infty }\frac{1}{\ln(n+2)}=0$, so 1 must hold.
To prove 2:
$\sum_{j=0}^n |\frac{1}{\ln(n+3)}- \frac{1}{\ln(n+2)}|$
$=\sum_{j=0}^n\left( \frac{1}{\ln(j+1)}-\frac{1}{\ln(j+2)} \right)$
=$\sum_{j=1}^{n+1} \frac{1}{\ln(j+1)}-\sum_{j=0}^n\frac{1}{\ln(j+1)}$
$= \frac{1}{\ln(j+2)}-\frac{1}{\ln j+0}$
$\lim_{ n \to \infty }=a_{0}$, thus 2 holds 

3: 
$\sum_{j=0}^n|b_{j}|\leq1 \forall n \in \mathbb{N}$
Thus this sequence must converge. 

Prove $\sum_{n=0}^\infty \frac{\cos(n+1)}{n+1}$ converges. 