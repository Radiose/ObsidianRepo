If you have $N$ independent, and identically distributed random variables $W_{1},\dots W_{N}$, taking values in $[0,1]$, with $\mathbb{E}(W_{i})=\mu$, then for every $\epsilon>0$, $\mathbb{P}\left( |\frac{1}{N}\sum_{i=1}^N W_{i}-\mu|>\epsilon \right)\leq 2e^{-2N\epsilon^2  }$

This goes to $0$ very fast. In other words, **the sample average of bounded, independent, identically distributed quantities is close to its expectation, and the probability of being far away decays exponentially in $N$.** 

The bound as a function of the sample size $N$:
![[Pasted image 20260813093426.png]]

Importantly, to half $\epsilon$, we need $4\times$ the amount of data.