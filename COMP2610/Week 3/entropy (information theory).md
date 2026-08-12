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



# ![[Entropy of a Bernoulli trial]]
# Maximised entropy 
This occurs when the distribution is a [[Uniform density and distribution|uniform distribution]].
Formally, denote $p_{i}$ to be the probability of a random variable taking state $i \in \{ 1,2,\dots,|\mathcal{X}| \}$
Denote the [[vector]] of probabilities $\mathbf{p}$. Entropy is maximum when $\mathbf{p}$ is uniform. 


