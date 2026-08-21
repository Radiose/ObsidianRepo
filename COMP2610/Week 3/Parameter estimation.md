---
aliases:
  - likelihood function
---
# Maximum likelihood estimation

Consider the set of observations $\mathcal{D}=\{ x_{1},\dots,x_{N} \}$ with $x_{i}\in \{ 0,1 \}$
Each observation is the outcome of a [[random variable]] $X$, with a binomial distribution.
Say we observe $$
\mathcal{D} = \{0, 0, 0, 1, 0, 0, 1, 0, 0, 0\}$$
If we were to assume that $\theta=\frac{1}{5}$, then we'd get
$$
\begin{aligned}
p(\mathcal{D} \mid \theta) &= \prod_{i=1}^{10} p(x_i \mid \theta) \\
&= \left(\frac{1}{5}\right)^2 \cdot \left(\frac{4}{5}\right)^8 \\
&\approx 0.007
\end{aligned}$$

We can write down how likely $\mathcal{D}$ is under the Bernoulli model. Assuming [[Independent event|independent]] observations:
$$
p(\mathcal{D} \mid \theta) = \prod_{i=1}^{N} p(x_i \mid \theta) = \prod_{i=1}^{N} \theta^{x_i} (1-\theta)^{1-x_i}$$
**We call $L(\theta)=p(\mathcal{D}|\theta)$ the likelihood function**. 
What our goal is to do is determine the probability of the thing we actually saw be given that $\theta$ is true. 




Maximising $p(\mathcal{D}|\theta)$ is easier if we use the logarithm = $\log(p(\mathcal{D}|\theta))$
$$=\sum_{i=1}^N[x_{i}\log \theta+(1-x_{i})\log(1-\theta)]$$ This is because log of a product is sum of components. 
Setting $\frac{d\mathcal{L}}{d\theta}=0$, we obtain
$\theta_{ML}=\frac{1}{n}\sum_{i=1}^N x_{i}$ - a very simple answer. 
However, if we use some really small [[Sample space]], this is a bad idea. We have overfitting. 


# Comp3670

Our goal here for our parametric methods is to get the $\theta$ that maximises the likelihood function. This is the idea behind maximum likelihood estimation. 

## The guarantees of MLE 
If we got the correct family, $\hat{\theta}$  converges to to $\theta^*$ as $N$ grows, and no other estimator is asymptotically more precise. It extracts everything the sample contains. 

However, if its wrong, it will still converge to the member of the family closest to the truth, and the procedure doesn't notice. This is another way to view an [[hypothesis set|approximation error]]. 

# Bayesian version
Using [[Bayes theorem|bayesian inference]] provides a much better way. 

Recall that $$
\underbrace{p(\theta \mid X)}_{\text{posterior}} = \frac{\overbrace{p(X \mid \theta)}^{\text{likelihood}}\ \overbrace{p(\theta)}^{\text{prior}}}{\underbrace{p(X)}_{\text{evidence}}}
$$
We need to find some good way to express the prior. It is mathematically a good idea to express it as a **beta distribution**.

$Beta(\theta|a,b)=\frac{1}{Z(a,b)}\theta^{a-1}(1-\theta)^{b-1}$, where $Z(a,b)$ is a suitable normaliser.
We can fine tune $a,b$ to reflect our belief in the likely values of $\theta$.
We can see below some examples. 
![[Pasted image 20260811162138.png|420]]

Recall that for $\mathcal{D}=\{ x_{0},x_{1},\dots,x_{m} \}$, the likelihood under a [[the Bernoulli distribution|Bernoulli]] model is:
$$
p(\mathcal{D} \mid \theta) = \theta^{m} (1-\theta)^{\ell},
$$
	*Notation:* $\sharp(\cdot)$ means "count of" — $\sharp(x=1)$ is the number of observations equal to $1$, $\sharp(x=0)$ the number equal to $0$.
	$\stackrel{\text{def}}{=}$ means "defined as," flagging that $\ell := N-m$ is a naming choice, not a derived fact.



$$
\textit{For the prior } p(\theta \mid a, b) = \text{Beta}(\theta \mid a, b) \text{ we can obtain the posterior:}
$$

$$
\begin{aligned}
p(\theta \mid \mathcal{D}, a, b) &= \frac{p(\mathcal{D} \mid \theta)\, p(\theta \mid a, b)}{p(\mathcal{D} \mid a, b)} \\[6pt]
&= \frac{p(\mathcal{D} \mid \theta)\, p(\theta \mid a, b)}{\int_0^1 p(\mathcal{D} \mid \theta)\, p(\theta \mid a, b)\, d\theta} \\[6pt]
&= \text{Beta}(\theta \mid m + a, \ell + b)
\end{aligned}
$$

# Maximising the posterior

We denote $\theta_{MAP}$ as the $\theta$ that will maximise the posterior $p(\theta|\mathcal{D})$

One can show that

$$
\theta_{\text{MAP}} = \frac{m + a - 1}{N + a + b - 2}
$$

comparing to the estimate that did not use any prior,

$$
\theta_{\text{ML}} = \frac{m}{N}
$$
