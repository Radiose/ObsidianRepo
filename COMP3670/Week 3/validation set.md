---
aliases:
  - empirical generalisation gap
---
This is a set we use to score each [[model selection|candidate model]] on their accuracy.



We fit $\hat{h}_{i}$ on the training part, using our candidate model $\mathcal{M}_{i}$ for $i=1,\dots ,n$. So for each candidate model, we get the smallest possible hypothesis, and then select the model with the least error. By fitting, we mean selecting the hypothesis with the lowest in sample error.


We then score it on the validation part. 


$E_{val}(\hat{h}_{i})=\frac{1}{K}\sum_{j \in validation}\ell((\mathbf{x_{j}},y_{j}),\hat{h}_{i})$

We then select the model with the smallest validation error. 

## The key point with a validation set 
$\hat{h}_{i}$ was found without the validation data, so it is effectively a fixed hypothesis. Because of this, we can directly apply [[Hoeffdings inequality]].

Importantly, we do not have a complexity term. The size of each $\mathcal{M}_{i}$ is irrelevant, only $K$ matters, where $K$ is the $N$ for the validation set. 

$$E_{ out}(\hat{h}_{i})  \leq E_{val}(\hat{h}_{i})  +\sqrt{ \frac{1}{2K}\log \frac{2n}{\delta} }$$

(note that we use n in the $\log$ term as another union bound idea for each model rather than hypothesis ).

# The validation split dilemma
The problem is that a $K$ too small will provide an unreliable estimate, and the wrong model may be selected. But too large is also a problem, as the $\hat{h}_{i}$ that is chosen may not be the most effective one. 
A common practical choice is $K=\frac{N}{5}$.

Once the model has been selected, we refit it on the entire dataset. This can only help, as selection has already been made. 


We should additionally note however, that this validation process is only effective if we use a small quantity of models. 
If we compare too many models, we will be doing something similar to the training error problems. We will not be learning something significant, but instead we will just have a significant quantity of models that makes it likely one will fit by luck. 



# The validation curve
![[Pasted image 20260820182904.png]]

The gap between these two is known as the empirical generalisation gap. 


![[Cross validation]]

![[Pasted image 20260820185427.png]]