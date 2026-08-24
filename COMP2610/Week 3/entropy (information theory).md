---
aliases:
  - entropy
---
let $X$ be a discrete [[random variable]] with probability outcomes $\mathcal{X}$.
The **Entropy** of $X$ is the average [[information]] content of the outcomes, calculated using the [[random variable|expected value]].
$$
\begin{aligned}
H(X) &= \mathbb{E}_x[h(x)] \\
&= \sum_x p(x) \cdot \log_2 \frac{1}{p(x)} \\
&= -\sum_x p(x) \log_2 p(x)
\end{aligned}
$$
we define $0\log 0\equiv \lim_{ p \to 0 }p\log(p)=0$.

There is not alot of overlap between the entropy in information theory and the entropy found in thermodynamics and physics. 


## Properties of entropy 
$H(x)\geq 0$
$H_{b}(X)=\log_{b}(a)H_{a}(X)$

The entropy of some random variable does not depend on the outcomes of its values, only the probabilities of them. Contrast this with the [[random variable|expected value]] which is built off the outcomes of the values of the random variable. The more peaky some distribution is, the higher the entropy. 


![[decomposability of entropy]]


# Entropy as a lower bound 
This is an essential property of entropy in information theory. In general, entropy acts as a lower bound on the average number of bits to transmit the state of a random variable. 

### Intuition 
Suppose you wanted to communicate what horse has one a race in the most efficient way possible. 
Assume that only the following horses participated in the last race: $\{acer, babe, cactus, daisy\}$.

The corresponding probabilities of winning are given by:

$$
p(X=a) = \frac{1}{2} \quad p(X=b) = \frac{1}{4} \quad p(X=c) = \frac{1}{8} \quad p(X=d) = \frac{1}{8}.
$$

You want to determine which horse won the race with the minimum number of yes/no questions:

As $a$ is the most likely, we first ask if $a$ won. 
![[Pasted image 20260812165328.png|431]]
The image above shows the question asking process. 

The entropy of this random variable determines a lower bound for the minimum number of binary questions:

$$
H_2(X) = -\left(\frac{1}{2}\log_2\frac{1}{2} + \frac{1}{4}\log_2\frac{1}{4} + \frac{1}{8}\log_2\frac{1}{8} + \frac{1}{8}\log_2\frac{1}{8}\right) = 1.75 \text{ bits.}
$$

This is in fact the minimum expected number of binary questions. **In general, this number lies between $H(X)$ and $H(X) + 1$**


# ![[Entropy of a Bernoulli trial]]
# Maximised entropy 
This occurs when the distribution is a [[Uniform density and distribution|uniform distribution]].
Formally, denote $p_{i}$ to be the probability of a random variable taking state $i \in \{ 1,2,\dots,|\mathcal{X}| \}$
Denote the [[vector]] of probabilities $\mathbf{p}$. Entropy is maximum when $\mathbf{p}$ is uniform. 



# Joint, conditional entropy and the chain rule 

![[joint entropy]]

![[conditional entropy]]
