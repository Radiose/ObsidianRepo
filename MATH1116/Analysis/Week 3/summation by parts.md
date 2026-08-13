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
Let $$