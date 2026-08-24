---
aliases:
  - the chain rule(entropy)
---
The **joint entropy** $H(X, Y)$ of a pair of discrete random variables with joint distribution $p(X, Y)$ is given by:

$$
\begin{aligned}
H(X, Y) &= \mathbb{E}_{X,Y}\left[\log \frac{1}{p(X,Y)}\right] \\
&= \sum_{x \in \mathcal{X}} \sum_{y \in \mathcal{Y}} p(x,y) \log \frac{1}{p(x,y)}
\end{aligned}
$$
assume this is $\log_{2}$.

If $X$ and $Y$ are statistically [[Independent event|independent]],
we have that:

$$
\begin{aligned}
H(X,Y) &= \sum_{x \in \mathcal{X}} \sum_{y \in \mathcal{Y}} p(x,y) \log \frac{1}{p(x,y)} \\
&= -\sum_{x \in \mathcal{X}} \sum_{y \in \mathcal{Y}} p(x)p(y)\big[\log p(x) + \log p(y)\big] \quad \text{as } p(x,y) = p(x)p(y) \\
&= -\sum_{x \in \mathcal{X}} p(x)\log p(x) \underbrace{\sum_{y \in \mathcal{Y}} p(y)}_{1} - \sum_{y \in \mathcal{Y}} p(y)\log p(y) \underbrace{\sum_{x \in \mathcal{X}} p(x)}_{1} \\
&= \sum_{x \in \mathcal{X}} p(x) \log \frac{1}{p(x)} + \sum_{y \in \mathcal{Y}} p(y) \log \frac{1}{p(y)} \\
&= H(X) + H(Y)
\end{aligned}
$$
The second line is where independence hypothesis is used. 


## The chain rule 

The joint entropy can be written as:

$$
\begin{aligned}
H(X,Y) &= -\sum_{x \in \mathcal{X}} \sum_{y \in \mathcal{Y}} p(x,y) \log p(x,y) \\
&= -\sum_{x \in \mathcal{X}} \sum_{y \in \mathcal{Y}} p(x,y)\big[\log p(x) + \log p(y|x)\big] \\
&= -\sum_{x \in \mathcal{X}} \log p(x) \underbrace{\sum_{y \in \mathcal{Y}} p(x,y)}_{p(x)} - \sum_{x \in \mathcal{X}} \sum_{y \in \mathcal{Y}} p(x,y) \log p(y|x)
\end{aligned}
$$

$$
H(X,Y) = H(X) + H(Y|X) = H(Y) + H(X|Y)
$$
So, the joint uncertainty of $X$ and $Y$ is the uncertainty of $X$, plus the uncertainty of $Y$, given $X$. 



# Graph 
Below we can see the relationship between joint entropy, [[conditional entropy]], [[mutual information]]. 
![[Pasted image 20260824162811.png]]