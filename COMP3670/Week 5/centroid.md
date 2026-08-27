for $\mathbf{x}_{1},\dots,\mathbf{x_{n}}$, their centroid is $$\mathbf{m}=\frac{1}{n}\sum_{i=1}^n x_{i}$$So, basically just the mean of the [[vector]] set coordinate wise. 


# Lemma 

Let $\mathbf{m}$ be the centroid of $\mathbf{x}_{1},\dots,\mathbf{x_{n}}$. $\forall \mathbf{c}\in \mathbb{R}^d$, $$\sum_{i=1}^n||\mathbf{x_{i}}-\mathbf{c}||^2_{2}=\left( \sum_{i=1}^n ||\mathbf{x}_{i}-\mathbf{m}||_{2}^2 \right) + n ||\mathbf{m}-\mathbf{c}||_{2}^2$$
Basically, the centroid will minimise the sum of squared distances to the datapoints. 