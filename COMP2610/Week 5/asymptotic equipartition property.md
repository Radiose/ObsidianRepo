# Informal 
As $N \to \infty$, $\log_{2}P(x_{1},\dots,x_{n})$ is close to $-NH(X)$ with high probability 

For large block sizes, almost all sequences are in the [[typical set]]. 

# Formally

If $x_1, x_2, \ldots$ are i.i.d. with distribution $P$ then, in probability,
$$-\frac{1}{N}\log_2 P(x_1,\ldots,x_N) \to H(X).$$

In precise language:
$$(\forall \beta > 0) \lim_{N\to\infty} p\left(\left|-\frac{1}{N}\log_2 P(x_1,\ldots,x_N) - H(X)\right| < \beta\right) = 1.$$
Note how closely this is related to the concept of [[typical set]].


### Proof
Since $x_1, \ldots, x_N$ are independent,
$$-\frac{1}{N}\log p(x_1,\ldots,x_N) = -\frac{1}{n}\log \prod_{n=1}^N p(x_n)$$
$$= -\frac{1}{N}\sum_{n=1}^N \log p(x_n).$$

Let $Y = -\log p(X)$ and $y_n = -\log p(x_n)$. Then, $y_n \sim Y$, and
$$\mathbb{E}[Y] = H(X).$$

But then by the law of large numbers,
$$(\forall \beta > 0) \lim_{N\to\infty} p\left(\left|\frac{1}{N}\sum_{n=1}^N y_n - H(X)\right| > \beta\right) = 0.$$
