---
aliases:
  - expected length
---
When a code is [[source code|uniform]], the length of a message $N$ is trivial to compute. However, with [[source code|variable length code]]s, the length of $N$ outcomes will depend on the outcomes we observe. 


We aim to determine what the average length of a message we can expect is? 
This can be determined with an [[random variable|expected value]], similar to the one used in probability theory. 

# Definition 
The expected length of a code is $C$ for [[ensemble]] $X$, with $A_{X}=\{ a_{1},\dots,a_{n} \}$ and $\mathcal{P}_{X}=\{ p_{1},\dots,p_{n} \}$ is given by $$L(C,X)=\mathbb{E}[\ell(x)]=\sum_{x \in \mathcal{A}_{x}}p(x)\ell(x)=\sum_{i=1}^lp_{i}\ell_{i}$$
The [[Kraft inequality]] can be used to convert the tuple of lengths $\{ \ell_{1},\dots,\ell_{I} \}$ to a probability vector that sums to one. 

Given code lengths $\ell_{1},\dots,\ell_{I}$ such that $\sum_{i=1}^I 2^{-2\ell_{i}}\leq {1}$, we define $\mathbf{q}=\{ q_{1},\dots q_{I} \}$, the probabilities for $\ell$, by $$q_{i}=\frac{2^{-\ell_{1}}}{z}$$ where $z=\sum_{i}2^{-\ell_{1}}$.

Ensure that $q_{i}$ satisfy $\sum_{i} q_{i}=1$
# Minimizing the expected code length 
