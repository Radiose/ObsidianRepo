Note that we consider blocks of outcomes as a method to describe [[sequence]]s.

![[Pasted image 20260826172741.png]]



Let $X$ be a single [[ensemble]]. The [[extended ensemble]] of blocks of size $N$ is denoted $X^N$. Outcomes from $X^N$ are denoted $\mathbf{x}=(x_{1},x_{2},\dots,x_{N})$
The probability of $\mathbf{x}$ is denoted to be $P(\mathbf{x})=P(x_{1})P(x_{2})\dots P(x_{N})$


# Example 

Let $X$ be an ensemble with outcomes $\mathcal{A}_X = \{\text{h}, \text{t}\}$ with $p_h = 0.9$ and $p_t = 0.1$.

Consider $X^4$ — i.e., 4 flips of the coin.
$$\mathcal{A}_{X^4} = \{\text{hhhh}, \text{hhht}, \text{hhth}, \ldots, \text{tttt}\}$$
Suppose the probability of a head is 0.9, and the probability of tails is 0.1
$P(hhhh)=(0.9)^4$
$P(tttt)=(0.1)^4$

# Entropy of [[extended ensemble]]s
We can view $X^4$ as comprising 4 independent [[random variable]]s based on the [[ensemble]] $X$. Recall [[entropy (information theory)|entropy]] is additive for [[Independent event|independent]] random variables. 

Thus, $H(X^4)=4(H(X)) = 4 \cdot (-0.9 \log 0.9   -0.1 \log 0.1)$


