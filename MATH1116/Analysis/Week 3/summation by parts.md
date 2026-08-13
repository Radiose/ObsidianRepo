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
