# Statement 
For any ensemble $X$, there exists a [[prefix code]] $C$ such that $H(X)\leq L(C,X)< H(X)+1$

In particular, [[Shannon code]]s have [[expected code length]] within $1$ bit of the [[entropy (information theory)|entropy]].


Note that since $\left[ x \right]$ is the smallest integer bigger than or equal to $x$, we have that $x \leq [x]<x+1$
Thus, creating a [[Shannon code]] $C$ for $\mathbf{p}=\{ p_{1},\dots,p_{n} \}$ with $\ell_{i}= \left\lceil  \log_{2} \frac{1}{p_{i}}  \right\rceil< \log_{2} \frac{1}{p_{i}}+1$ will satisfy $$
\begin{aligned}
L(C,X) = \sum_i p_i \ell_i &< \sum_i p_i \left(\log_2 \frac{1}{p_i} + 1\right) \\
&= \sum_i p_i \log_2 \frac{1}{p_i} + \sum_i p_i \\
&= H(X) + 1
\end{aligned}$$

Furthermore, since $\ell_i \ge -\log_2 p_i$ we have $2^{-\ell_i} \le 2^{\log_2 p_i} = p_i$, so $\sum_i 2^{-\ell_i} \le \sum_i p_i = 1$. By Kraft there is a *prefix code* with lengths $\ell_i$.

This shows basically that entropy is lower bound for compression. 

Note that Huffman coding is the only way to get a guaranteed optimal [[prefix code]].

