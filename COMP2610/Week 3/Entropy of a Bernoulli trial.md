Let $X \in \{0, 1\}$ with $X \sim \text{Bern}(X|\theta)$

Then,

$$
p(X = 0) = 1 - \theta
$$
$$
p(X = 1) = \theta
$$

So, the entropy of a Bernoulli random variable is

$$
\begin{aligned}
H(X) &= -\sum_{x \in \{0,1\}} p(x) \cdot \log_2 p(x) \\
&= -\theta \log_2 \theta - (1-\theta)\log_2(1-\theta)
\end{aligned}
$$
![[Pasted image 20260812162237.png]]

Here we have entropy as $\theta$ varies. As you can see, the entropy is the highest when all are equally unlikely, and non-existent when a result is guaranteed. 

