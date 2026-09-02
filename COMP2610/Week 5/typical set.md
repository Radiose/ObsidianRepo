# Motivation 

With a probability of heads $p_{h}=.75$, what is the probability distribution for $X^2$
![[Pasted image 20260826185228.png]]

As N increases, there is an increasing spread of probabilities. The most likely individual sequence will always be the all heads one. However, for $N=4$, the most likely sequence **type** is 3 heads, and 1 tail. 


A natural question to ask is *how often does each symbol appear in a sequence $\mathbf{x}$ from $X^N$*?
Intuitively, in a sequence of length $N$, let $a_{i}$ appear $n_{i}$ times,

 Then **in expectation**
$$n_i \approx N \cdot P(a_i)$$

Note $p_i = P(a_i)$, and
$$P(\mathbf{x}) = P(a_1)^{n_1}P(a_2)^{n_2}\cdots P(a_I)^{n_I} \approx p_1^{Np_1}p_2^{Np_2}\cdots p_I^{Np_I}$$

So the *information content* $-\log_2 P(\mathbf{x})$ of that sequence is approximately
$$-p_1 N \log_2 p_1 - \cdots - p_I N \log_2 p_I = -N\sum_{i=1}^I p_i \log_2 p_i = NH(X)$$

# Definition 
We want to consider elements $\mathbf{x}$ that have $-\log_{2}P(\mathbf{x})$ close to $NH(X)$

For closeness $\beta > 0$, the typical set $T_{N\beta}$ for $X^N$ is 
$$
\begin{aligned}
T_{N\beta} &\overset{\text{def}}{=} \left\{ \mathbf{x} : \left| -\log_2 P(\mathbf{x}) - NH(X) \right| < N\beta \right\} \\
&= \left\{ \mathbf{x} : \left| -\frac{1}{N}\log_2 P(\mathbf{x}) - H(X) \right| < \beta \right\}
\end{aligned}$$

Where $\frac{1}{N}\log_{2}p(x)$ is the average information content, and H(x) is the entropy. 

The name typical is used because each $\mathbf{x}\in T_{N\beta}$ will have roughly $p_{1}N$ occurrences of symbol $a_{1}$, $p_{2}N$ of $a_{2},\dots p_{k}N$ of $a_{k}$

![[Pasted image 20260826191546.png]]


Above are randomly drawn sequences from $P(1)=0.1$

# Properties 
# Equiprobability

Typical sequences are nearly equiprobable: Every $\mathbf{x} \in T_{N\beta}$ has
$$2^{-N(H(X)+\beta)} \leq P(\mathbf{x}) \leq 2^{-N(H(X)-\beta)}.$$

Variation is small when $\beta$ is small


### Bound of cardinality
Number of sequences in the typical set: For any $N, \beta$,
$$|T_{N\beta}| \leq 2^{N(H(X)+\beta)}.$$
The [[cardinality]] is bound.


### Most likely sequence 

The most likely sequence may not belong to the [[typical set]]

![[Pasted image 20260826192556.png]]


