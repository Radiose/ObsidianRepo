---
aliases:
  - KL divergence
---
If a [[random variable]] has a distribution $p$, there exists an encoding with an average length of $H(p)$ bits. This is just the [[entropy (information theory)]].

However, sometimes, we may use the wrong encoding. If the true distribution is $p$, but we assume it to be $q$, then it turns out we will need to use $H(p)+D_{kl}(p ||q)$ bits, where $D_{kl}(p||q)$ is a measure of distance between $p$ and $q$. 


# Definition 
$D_{kl}(p||q)=\mathbb{E}_{p}\left[\log \frac{p(X)}{q(x)} \right]$
This is because logarithms have subtraction converted to division. That way, we can measure the distance with division. 

We define edge cases here. 
$0 \log \frac{0}{0}:=0$, $0 \log \frac{0}{p}:=0$, $p \log \frac{p}{0}:=\infty$

# Properties 
Always $\geq {0}$
Not [[symmetric relation]]. 
$D_{kl}(p ||q)=0 \iff p=q$


## With a [[Uniform density and distribution|uniform distribution]]

This is when $q(x)=\frac{1}{|\mathcal{X}|}$

$$
D_{\text{KL}}(p\|q) = \sum_{x \in \mathcal{X}} p(x) \log \frac{p(x)}{q(x)}
$$

$$
= \sum_{x \in \mathcal{X}} p(x) \cdot (\log p(x) + \log |\mathcal{X}|)
$$

$$
= -H(X) + \sum_{x \in \mathcal{X}} p(x) \cdot \log |\mathcal{X}|
$$

$$
= -H(X) + \log |\mathcal{X}|.
$$
So, because the [[entropy (information theory)|entropy]] of a uniform distribution is $\log_{2}X$, this matches our intuition. 


## Another example 
Let $X \in \{ 0,1 \}$ IE, it is a [[the Bernoulli distribution|Bernoulli trial]]. 
$p(X=1)=\theta_{p}$
$q(X=1)=\theta_{q}$


$$
\begin{aligned}
D_{\text{KL}}(p\|q) &= \theta_p \log \frac{\theta_p}{\theta_q} + (1-\theta_p) \log \frac{1-\theta_p}{1-\theta_q} \\
&= \frac{1}{2} \log \frac{\frac{1}{2}}{\frac{1}{4}} + \frac{1}{2} \log \frac{\frac{1}{2}}{\frac{3}{4}} = 1 - \frac{1}{2} \log 3 \approx 0.2075 \text{ bits}
\end{aligned}
$$

$$
\begin{aligned}
D_{\text{KL}}(q\|p) &= \theta_q \log \frac{\theta_q}{\theta_p} + (1-\theta_q) \log \frac{1-\theta_q}{1-\theta_p} \\
&= \frac{1}{4} \log \frac{\frac{1}{4}}{\frac{1}{2}} + \frac{3}{4} \log \frac{\frac{3}{4}}{\frac{1}{2}} = -1 + \frac{3}{4} \log 3 \approx 0.1887 \text{ bits}
\end{aligned}
$$
This is why its unsymmetric. 



