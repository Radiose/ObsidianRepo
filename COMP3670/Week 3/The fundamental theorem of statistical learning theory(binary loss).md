[[Empirical risk minimisation]] on some $\mathcal{H}$ is consistent for every distribution $P \iff d_{VC}(\mathcal{H})<\infty$.

Consistent means: $E_{out}(\hat{h}_{N}) \to E_{out}(h^*)$ as $N \to \infty$, with probability 1 over all possible samples. 

Basically, the idea is that with enough data, we can falsify all hypothesis. 

How much data do we need then to get an ideal hypothesis. 

Given a tolerance $\epsilon$, and a confidence $1-\delta$, how how many samples do I need? 
Solving from the [[Empirical risk minimisation]], 
$8(N+1)^v e^{-N\epsilon^2/32}\le \delta$ does not depend on $P$.

![[PAC learnable]]

# Basically 
$\mathcal{H}$ is PAC learnable by ERM $\iff$ $d_{VC}(\mathcal{H})<\infty \iff \mathcal{H}$ is falsifiable.
The sample complexity is obtained from the $VC$ bound, where it grows like 

$N_{\mathcal{H}}(\epsilon,\delta) \textasciitilde \frac{1}{\epsilon^2}\left( v\log\left( \frac{1}{\epsilon} +\log\left( \frac{1}{\delta} \right)\right) \right)$

So basically, this proves that we have some guarantee that with sufficient samples, we can minimise the out of sample error. 

If the model is falsifiable(through its $VC$ dimension), then with enough data, the hypothesis returned by the [[Empirical risk minimisation]] is with high probability, as good as the best hypothesis in $\mathcal{H}$. We quantify induction. 


# Properties
Linear in complexity $v$
Quadratic in the accuracy $\epsilon$
logarithmic in the confidence. 
This is the precise form of the probabilistic answer to [[Humes problem of induction]].

# Shortcomings 
The $VC$ bound holds for any distribution $P$. This makes it assume worst case alot of times. Real data is often smooth, redundant and structured. The actual gap is far smaller than the bound. 

2: sample sizes are unrealistic.

3: This is all for binary [[loss function]], rather than regression. This works only because loss is bounded between $\{0,1\}$.


