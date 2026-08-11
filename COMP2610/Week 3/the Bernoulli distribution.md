---
aliases:
  - Bernoulli trial
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
The [[Random variable|expected value]] (or mean) is given by 
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

Parameter estimation
Consider the set of observations $\mathcal{D}=\{ x_{1},\dots,x_{N} \}$ with $x_{i}\in \{ 0,1 \}$
Each observation is the outcome of a [[Random variable]] $X$, with a binomial distribution.
Say we observe $$
\mathcal{D} = \{0, 0, 0, 1, 0, 0, 1, 0, 0, 0\}
$$
If we were to assume that $\theta=\frac{1}{5}$, then we'd get
$$
\begin{aligned}
p(\mathcal{D} \mid \theta) &= \prod_{i=1}^{10} p(x_i \mid \theta) \\
&= \left(\frac{1}{5}\right)^2 \cdot \left(\frac{4}{5}\right)^8 \\
&\approx 0.007
\end{aligned}
$$

We can write down how likely $\mathcal{D}$ is under the Bernoulli model. Assuming [[Independent event|independent]] observations:
$$
p(\mathcal{D} \mid \theta) = \prod_{i=1}^{N} p(x_i \mid \theta) = \prod_{i=1}^{N} \theta^{x_i} (1-\theta)^{1-x_i}
$$
We call $L(\theta)=p(\mathcal{D}|\theta)$ the likelihood function. 


Maximising $p(\mathcal{D}|\theta)$ is 