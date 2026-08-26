suppose there are $X_{1},\dots,X_{n}$ [[random variable]]s [[Independent event|independent]] and identically distributed. 

Let $\mathbb{E}[X_{i}]=\mu$ (all are identically distributed so same mean)

Suppose $$\mathbb{V}[X_{i}]<\infty$$
Define $$\bar{X}_{n}=\frac{X_{1}+\dots+X_{n}}{n}$$
Then, for any $\epsilon>0$, $$\lim_{ n \to \infty }p(|\bar{X}_{n}-\mu|>\epsilon)=0$$
The probability of the empirical success frequency converges to the [[random variable|expected value]].

### Proof 
Since the $X_i$'s are identically distributed,
$$
\mathbb{E}[\bar{X}_n] = \mu.
$$

Since the $X_i$'s are independent,
$$
\begin{aligned}
\mathbb{V}[\bar{X}_n] &= \mathbb{V}\left[\frac{X_1 + \cdots + X_n}{n}\right] \\
&= \frac{\mathbb{V}[X_1 + \cdots + X_n]}{n^2} \\
&= \frac{n\sigma^2}{n^2} \\
&= \frac{\sigma^2}{n}.
\end{aligned}
$$


Applying Chebyshev's inequality to $\bar{X}_n$,
$$
\begin{aligned}
p(|\bar{X}_n - \mu| \geq \epsilon) &\leq \frac{\mathbb{V}[\bar{X}_n]}{\epsilon^2} \\
&= \frac{\sigma^2}{n\epsilon^2}.
\end{aligned}
$$

For any fixed $\epsilon > 0$, as $n \to \infty$, the right hand side $\to 0$.

Thus,
$$
p(|\bar{X}_n - \mu| < \epsilon) \to 1.
$$