There are two main forms of conditional entropy 
The conditional entropy of $Y$ given $X=x$. This is just the entropy of the probability distribution $p(Y|X=x)$


$$
H(Y|X=x) = \sum_{y \in \mathcal{Y}} p(y|X=x) \log \frac{1}{p(y|X=x)}
$$



The conditional entropy of $Y$ given $X$, is the average over $X$ of the conditional entropy of $Y$ given $X = x$:

$$
\begin{aligned}
H(Y|X) &= \sum_{x \in \mathcal{X}} p(x) H(Y|X=x) \\
&= \sum_{x \in \mathcal{X}} p(x) \sum_{y \in \mathcal{Y}} p(y|x) \log \frac{1}{p(y|x)}
\end{aligned}
$$
This one means the average uncertainty of $Y$, given that we know everything about $X$.

We can re-write the conditional entropy as follows:

$$
\begin{aligned}
H(Y|X) &= \sum_{x \in \mathcal{X}} p(x) \sum_{y \in \mathcal{Y}} p(y|x) \log \frac{1}{p(y|x)} \\
&= \sum_{x \in \mathcal{X}} \sum_{y \in \mathcal{Y}} p(x) p(y|x) \log \frac{1}{p(y|x)} \\
&= \sum_{x \in \mathcal{X}} \sum_{y \in \mathcal{Y}} p(x,y) \log \frac{1}{p(y|x)} \\
&= \mathbb{E}_{X,Y}\left[\log \frac{1}{p(Y|X)}\right]
\end{aligned}
$$
Note, that we are taking the expectation here with respect to the [[Joint probability]] distribution, rather than the conditional. 


![[information cannot hurt theorem]]