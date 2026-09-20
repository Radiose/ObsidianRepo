$y$ takes [[continuous function|continuous]] values rather than discrete. We treat $y$ as a continuous [[random variable]].
Some examples are $\mathcal{Y}=\mathbb{R},\mathcal{Y}=\mathbb{R}_{+},\mathcal{Y}=[a,b]$


Our [[loss function]] is the squared loss. 

The best possible predictor, and its loss are as follows below 

$$
f^*(\mathbf{x}) = \mathbb{E}[Y \mid \mathbf{X} = \mathbf{x}], \qquad E_{\text{out}}(f^*) = \mathbb{E}\left[\text{Var}(Y \mid \mathbf{X})\right]
$$

It is convenient to write the phenomenon as "signal plus noise":

$$
Y = f^*(\mathbf{X}) + \varepsilon, \qquad \mathbb{E}[\varepsilon \mid \mathbf{X}] = 0
$$

which is not an assumption: it is just the definition of $\varepsilon = Y - f^*(\mathbf{X})$


# ![[parametric regression]]