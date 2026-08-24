While [[relative entropy]] tells us how similar our distributions are, mutual information tells us how similar our [[random variable]]s are.

# Definition 

Let $X,Y$ be [[random variable]]s with joint distribution $p(X,Y)$ and [[marginal probability|marginal probabilities]] $p(X)$, $p(Y)$. 
The [[mutual information]] $I(X,Y)$ is the [[relative entropy]] between the joint distribution $p(X,Y)$ and the product distribution $p(X)p(Y)$. 
$$I(X;Y)=D_{KL}(p(X,Y)||p(X)p(Y))$$
$$=\sum_{x \in \mathcal{X}}\sum_{y \in \mathcal{Y}}p(x,y)\cdot \log \frac{p(x,y)}{p(x)p(y)}$$
If two [[random variable]]s are statistically [[Independent event|independent]], then the [[relative entropy|KL divergence]] will be 0.
We should note that mutual information is [[symmetric relation]], unlike KL divergence. 

Intuitively, how much [[information]] on average does $X$ tell about $Y$?




# Relationship between Entropy and mutual information 
We can rewrite the definition of mutual information as 
$$
\begin{aligned}
I(X;Y) &= \sum_{x \in \mathcal{X}} \sum_{y \in \mathcal{Y}} p(x,y) \log \frac{p(x,y)}{p(x)p(y)} \\
&= \sum_{x \in \mathcal{X}} \sum_{y \in \mathcal{Y}} p(x,y) \log \frac{p(x|y)}{p(x)} \\
&= -\sum_{x \in \mathcal{X}} \log p(x) \sum_{y \in \mathcal{Y}} p(x,y) - \left( -\sum_{x \in \mathcal{X}} \sum_{y \in \mathcal{Y}} p(x,y) \log p(x|y) \right) \\
&= H(X) - H(X|Y)
\end{aligned}
$$
The average reduction in the uncertainty of $X$, given the uncertainty of $Y$. 

self mutual information $I(X,X)=H(X)-H(X|X)=H(X)$


![[Conditional mutual information]]


joint [[mutual information]]
