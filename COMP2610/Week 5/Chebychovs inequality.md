Sometimes, [[Markov's inequality]] cannot be used for [[random variable]]s that take negative values. 

Additionally, it only tells uses the mean. We want to use the [[variance]] more.

# Definition 
Let $X$ be a [[random variable]] with $\mathbb{E}[X]<\infty$. Then, for any $\lambda >0$, $$p(|X-\mathbb{E}[X]| \geq \lambda) \leq \frac{\mathbb{V}[X]}{\lambda^2}$$
This bounds the probability of observing an unexpected outcome. The probability that $X$ is $\lambda$ distance from the mean is given by above.

# Corollary 
$$p(|X-\mathbb{E}(X)|\geq \lambda \cdot \sqrt{ \mathbb{V}[X] }) \leq \frac{1}{\lambda^2}$$
Observations are unlikely to occur several standard deviations away
The probability that $X$ is $\lambda$ standard deviations away from the mean.

### Proof

Define
$$
Y = (X - \mathbb{E}[X])^2.
$$

Then, by Markov's inequality, for any $\nu > 0$,
$$
p(Y \geq \nu) \leq \frac{\mathbb{E}[Y]}{\nu}.
$$

But,
$$
\mathbb{E}[Y] = \mathbb{V}[X].
$$

Also,
$$
Y \geq \nu \iff |X - \mathbb{E}[X]| \geq \sqrt{\nu}.
$$

Thus, setting $\lambda = \sqrt{\nu}$,
$$
p(|X - \mathbb{E}[X]| \geq \lambda) \leq \frac{\mathbb{V}[X]}{\lambda^2}.
$$

# Example 
Suppose we are flipping some coin $n$ times with bias $\theta,p(X=1)=\theta$

We flip the coin $n$ times, and observe $x_{1},\dots,x_{n} \in \{ 0,1 \}$
We use the maximum likelihood estimator of $\theta$ ( from the [[binomial distribution]]): $$\hat{\theta}=\frac{x_{1}+\dots+x_{n}}{n}$$we estimate how large n should be such that $p(|\hat{\theta}_{n}-\theta|\ge { 0}.05)\leq {0}.01$.  
1% probability with 5% error.  - the probability that the dif

So our goal here is to use [[Chebychovs inequality]] to this 
We use the basic version 

Observe that
$$
\mathbb{E}[\hat{\theta}_n] = \frac{\sum_{i=1}^n \mathbb{E}[x_i]}{n} = \theta
$$
$$
\mathbb{V}[\hat{\theta}_n] = \frac{\sum_{i=1}^n \mathbb{V}[x_i]}{n^2} = \frac{\theta(1-\theta)}{n}.
$$

Thus, applying Chebyshev's inequality to $\hat{\theta}_n$,
$$p(|\hat{\theta}_n - \theta| > 0.05) \leq \frac{\theta(1-\theta)}{(0.05)^2 \cdot n}.$$

We are guaranteed this is less than 0.01 if

$$p(|\hat{\theta}_n - \theta| > 0.05) \leq \frac{\theta(1-\theta)}{(0.05)^2 \cdot n}. <0.01$$

$$n \geq \frac{\theta(1-\theta)}{(0.05)^2(0.01)}.$$



When $\theta = 0.5$, $n \geq 10{,}000$
