If a [[random variable]] has a distribution $p$, there exists an encoding with an average length of $H(p)$ bits. This is just the [[entropy (information theory)]].

However, sometimes, we may use the wrong encoding. If the true distribution is $p$, but we assume it to be $q$, then it turns out we will need to use $H(p)+D_{kl}(p ||q)$ bits, where $D_{kl}(p||q)$ is a measure of distance between $p$ and $q$. 


# Definition 
$D_{kl}(p||q)=\mathbb{E}_{p}\left[\log \frac{p(X)}{q(x)} \right]$
This is because logarithms have subtraction converted to division. That way, we can measure the distance with division. 

We define edge cases here. 
$0 \log \frac{0}{0}:=0$, $0 \log \frac{0}{p}:=0$, $p \log \frac{q}{0}:=\infty$

