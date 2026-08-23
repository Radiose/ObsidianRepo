---
aliases:
  - surrogate loss
---
Cross [[entropy (information theory)|entropy]] [[loss function]]

For a hypothesis that outputs a probability $\eta(\mathbf{x})\in(0,1)$, rather that a label, 


$$
\ell((\mathbf{x}, y), \eta) = -y \log \eta(\mathbf{x}) - (1-y) \log\left(1 - \eta(\mathbf{x})\right)$$

- Read it: if $y=1$ we pay $-\log \eta(\mathbf{x})$, which is $0$ when we said "certainly 1" and $+\infty$ when we said "certainly 0". Symmetrically for $y=0$. If we say 


- So **maximum likelihood for the logistic model is [[Empirical risk minimisation]] with the cross-entropy loss**:

$$
\hat{\theta} = \underset{\theta}{\arg\max} \; \text{LL}(\theta) = \underset{\theta}{\arg\min} \; \frac{1}{N} \sum_{i=1}^{N} \ell\big((\mathbf{X}_i, Y_i), \eta(\cdot \mid \theta)\big)$$
## Necessity 
The binary [[loss function]] only returns whetehr a predicted label was right. It cannot handle hypothesis that reutnr the probability of the label one.

The [[cross entropy loss]] score scores the whole probability statement. A confident mistake is greatly punished, while a hesitant one is only mildly. This is what makes it useful for fitting a probability model. 

We obtain a new classifier. 
$$
\hat{h}(\mathbf{x}) = \mathbb{1}\left\{ \frac{1}{1 + e^{-\left(\sum_{j=1}^{d} \hat{w}_j x_j + \hat{w}_0\right)}} > 1/2 \right\} = \mathbb{1}\left\{ \sum_{j=1}^{d} \hat{w}_j x_j + \hat{w}_0 > 0 \right\}$$

This is basically just [[The perceptron]] model. We also call this a surrogate loss. This means that the logistic classifier is a linear classifier. 

In words, $\hat{h}$ is the linear classifier whos associated probability model makes the observes labels most likely. 
The probabilities themselves are often the real output. $\eta(x)=0.8$ is more useful to a clinician that class $1$.

# The hypothesis set 
