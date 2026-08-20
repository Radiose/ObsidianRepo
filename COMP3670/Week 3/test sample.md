This is a set of examples drawn from a distribution $P$ that is locked away at the start and looked at only once at the very end of [[supervised learning]].

Our $\hat{h}$ is produced only once, at the end of testing over our [[validation set]]. 

Because $\hat{h}$ is a single, fixed hypothesis, plain [[Hoeffdings inequality]] applies here. 
$$
|E_{\text{test}}(\hat{h}) - E_{\text{out}}(\hat{h})| \leq \sqrt{\frac{1}{2N_{\text{test}}} \log \frac{2}{\delta}}
$$

We are just doing verification. 

- **Example**. A classifier is evaluated on $N_{\text{test}} = 1000$ held-out examples and misclassifies 83 of them, so $E_{\text{test}}(\hat{h}) = 0.083$

- With $\delta = 0.05$ the error bar is $\sqrt{\frac{1}{2000} \log 40} \approx 0.043$, so with 95% confidence

$$
E_{\text{out}}(\hat{h}) \in [0.040,\ 0.126]
$$

- Note that this is **unbiased in both directions**: unlike $E_{\text{in}}$, the test error is as likely to be too pessimistic as too optimistic

- Note also how much sharper it is than the VC bound: no $d_{\text{VC}}$ appears, only $N_{\text{test}}$. **Measuring beats bounding** whenever we can afford to hold out data

- And note the cost: those 1000 examples were **not** used for training

# Warning 
Importantly, we can only use our test set once. The moment we look at the result and change something because of it, the test set has become a [[validation set]], and its purpose is void. If you must iterate, iterate over the [[validation set]]. 
![[Pasted image 20260820185410.png]]
