Suppose we perform $N$ independent Bernoulli trials. 
Each trial has $\theta$ probability of success. 
What is the distribution of the number of times that $X$=1?
	IE what is the amount of times we obtained $m$ heads? 
	What is the number of errors in the transmitted sequence?

Let $Y=\sum_{i=1}^N X_{i}$
where $X_{i} \textasciitilde bern(\theta)$
Then, $Y$ has a binomial distribution with parameters $N,\theta$:
$p(Y=m)=Bin(m|N,\theta)=\begin{pmatrix}N \\ m\end{pmatrix}\theta^m(1-\theta)^{n-m}$

[[Binomial theorem]].


[[random variable|expected value]] and [[variance]] of [[binomial distribution]]:
$$
\begin{aligned}
\mathbb{E}[Y] &= \sum_{m=0}^{N} m \cdot \text{Bin}(m \mid N, \theta) = N\theta \\[4pt]
\mathbb{V}[Y] &= \sum_{m=0}^{N} (m - \mathbb{E}[m])^2 \cdot \text{Bin}(m \mid N, \theta) = N\theta(1 - \theta)
\end{aligned}
$$
