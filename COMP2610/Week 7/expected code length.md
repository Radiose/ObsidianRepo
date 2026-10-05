---
aliases:
  - expected length
---
When a code is [[source code|uniform]], the length of a message $N$ is trivial to compute. However, with [[source code|variable length code]]s, the length of $N$ outcomes will depend on the outcomes we observe. 


We aim to determine what the average length of a message we can expect is? 
This can be determined with an [[random variable|expected value]], similar to the one used in probability theory. 

# Definition 
The expected length of a code is $C$ for [[ensemble]] $X$, with $A_{X}=\{ a_{1},\dots,a_{n} \}$ and $\mathcal{P}_{X}=\{ p_{1},\dots,p_{n} \}$ is given by $$L(C,X)=\mathbb{E}[\ell(x)]=\sum_{x \in \mathcal{A}_{x}}p(x)\ell(x)=\sum_{i=1}^lp_{i}\ell_{i}$$
The [[Kraft inequality]] 