# Motivation 
The basis of interval coding is to recover some of the issues with symbol codes, particularly the limitations listed [[Huffman coding#Use cases|here]]. 

# Building to it
Suppose $X$ is some [[ensemble]] with probabilities $p_{1},\dots,p_{\lvert X \rvert}$

Define the [[Cumulative probability distribution function]] $$F(x):=\sum_{i \leq x}p_{i}$$The modified cumulative distribution function is $$\overline{F(x)}=\sum_{i<x} p_{i}+\frac{1}{2}\cdot p(x)=F(x)-\frac{1}{2}\cdot p(x)$$
We can [[source code|losslessly code]] outcomes based on $\overline{F}(x)$
Note that $\overline{F}(x)$ serves as the midpoint of each jump up the CPDF 
![[Pasted image 20261014112208.png|516]]


However, we run into a problem quite quickly. 