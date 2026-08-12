---
aliases:
  - Bernoulli trial
  - Bernoulli
---
Consider a binary variable $X=\{ 0,1 \}$. Often, these outcomes are not equally likely, so we come up with some general way to model $X$. This is very useful for many things, including mainly successful vs unsuccessful events. 


The variable $X$ takes on the outcomes $1$, given by probability $\theta$, and $0$, given by probability $\theta-1$.
For higher values of $\theta$, it is more likely to see outcome 1 than 0. 
Obviously, $\theta \in[0,1]$. We denote $\theta$ to be the parameter. 

## Definition of Bernoulli dist. 
By definition, 
$p(X=1|\theta)=\theta$ - the probability that the random variable takes this value under the parameter $\theta$
$p(X=0|\theta)=1-\theta$

And more succinctly, $p(X=x|\theta)=bern(x|\theta)=\theta^x(1-\theta)^{1-x}$ .
The [[random variable|expected value]] (or mean) is given by 
$$
\mathbb{E}[X \mid \theta] = \sum_{x \in \{0,1\}} x \cdot p(x \mid \theta) = 1 \cdot p(X = 1 \mid \theta) + 0 \cdot p(X = 0 \mid \theta) = \theta
$$
[[variance]] is given by
$$
\begin{aligned}
\mathbb{V}[X \mid \theta] &= \mathbb{E}[(X - \mathbb{E}[X])^2] \\
&= \mathbb{E}[(X - \theta)^2] \\
&= (0 - \theta)^2 \cdot p(X = 0 \mid \theta) + (1 - \theta)^2 \cdot p(X = 1 \mid \theta) \\
&= \theta(1 - \theta)
\end{aligned}
$$
![[binomial distribution]]
![[Parameter estimation]]