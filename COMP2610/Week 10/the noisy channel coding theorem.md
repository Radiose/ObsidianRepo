# Motivation 
Ideally, we want our [[block code]] to have high [[rate of block code|rates]] for our channel code. Low rate implies we are being wasteful with channel use. 

At high rates, we run the risk of losing reliability.

## Reliability
![[reliability of block codes]]

# The noisy channel coding theorem (brief)
If $Q$ is a channel with [[channel capacity]] $C$, then the rate $R$ is [[achievable rate|achievable]] $\iff$ $R \leq C$
(the rate is no greater than the channel capacity)


## Intuition 
When a channel $Q$ is used $N$ times, we can view it as a something called an **extended channel**
![[extended channel]]


# Formal statement of the noisy channel coding theorem 
Thee statements:
1: Any rate $R<C$ is acheivable for $Q$
2: If probability of bit error $p_{B}:=\frac{p_{B}}{K}$ is acceptable, $(N,K)$ codes exist with rates $$\frac{K}{N} \leq R(p_{b})= \frac{C}{1-H_{2}(p_{b})}$$where $p_{B}$ is the average **block** error. 
3: For any $p$, we cannot achieve a rate greater than $R(p)$ with probability of bit error $p$.

Note that as $p_{b} \to \frac{1}{2},$ $R(p_{b}) \to + \infty$ while $p_{b} \to \{ 0,1 \}$ means that $R(p_{b})\to C$
