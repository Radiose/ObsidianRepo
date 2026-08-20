Recall that the [[target function]] in a binary classification problem is $$
f^{\star}(\mathbf{x}) = \mathbb{1}\{\eta(\mathbf{x}) > \tfrac{1}{2}\}, \qquad \eta(\mathbf{x}) = \mathbb{P}(Y = 1 \mid \mathbf{X} = \mathbf{x})$$
We have some alternative to [[Empirical risk minimisation]], where we aim to use the data to estimate $\eta$ and from there substitute the estimate into the classification rule. Basically, determine our [[conditional distribution]] to get a classifier. 

![[Pasted image 20260820190629.png]]

As we can see above, we assume some model for the distribution $P$, where we refer to a statistical model. When he have this, we return a rule for the target, and use a [[loss function]] only to evaluate our results. As you can see, its quite different to a *machine learning model.* 


This works when we have a good distributional model for our data. This is more of a statisticians route. 
A plug in rule does not minimise error. 

We have two families of methods to do these plug in rules.
For both, we have the same classifier, and the two families differ only in how $\eta$ is built.



![[parametric methods]]

![[nonparametric methods]]

