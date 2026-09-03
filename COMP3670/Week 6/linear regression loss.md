Let $\mathbf{X}\in \mathbb{R}^{n \times d}$ be a data [[matrix]]. Let $\mathbf{y} \in \mathbb{R}^n$ contain the targets, and let $\mathbf{w \in \mathbb{R}^d}$ be the weight [[vector]].
The predictions are $\mathbf{\hat{y}}=\mathbf{X}\mathbf{w}$
The mean squared error can be written as $$L(\mathbf{w})=\frac{1}{n}\sum_{i=1}^n (\mathbf{x_{i}}^T\mathbf{w}-\mathbf{y}_{i})^2=\frac{1}{n}||\mathbf{Xw-y}||_{2}^2$$
So you take the distance, and square it, and then get the mean.
