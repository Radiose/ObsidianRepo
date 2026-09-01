Let $X$ be an [[ensemble]] and for $0 \leq \delta \leq 1$, we define $S_{\delta}$ to be the **smallest** subset of $\mathcal{A}_{X}$ such that
$$P(x \in S_{\delta})\geq 1-\delta$$
So when $\delta=0$, there are no errors.

If we can uniformly code elements in $S_{\delta}$ and ignore all the elements, we can code [[sequence]]s with length $N$ with probability $(1-\delta)^N$. 
Additionally, the expected length will be $N\log_{2} |S_{\delta}|$



# Example 
We construct $S_{\delta }$ by removing elements in $X$ in ascending order of probability until we have reached $1-\delta$ threshold.

For example, ![[Pasted image 20260901130416.png]] given the distribution to the left, if we choose $\delta=0$, then the probability that $x$ is in $S_{\delta}$ has to be 1, so there is no error and $s_{\delta}$ has to include the entirety of $a-g$