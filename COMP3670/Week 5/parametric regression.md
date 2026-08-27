---
aliases:
  - nonparametric regression
---
[[parametric methods|parametric]] [[regression]]

currently regression is highly effected by noise in a sample. Our solution is as follows 

Assume a shape with finitely many unknowns.
Estimate $\theta$ and return the [[plug in rules|plug in]] predictor $\hat{h}(\mathbf{x})=h(\mathbf{x};\hat{\theta})$

The gap between what the predictor says at $\mathbf{X}_{i}$, and what we observed is called the residual $Y_{i}-h(\mathbf{X}_{i};\theta)$

[[Gauss least squares]] make the squared residuals as small as possible in total 
$$\hat{\theta} = \operatorname*{arg\,min}_{\theta \in \Theta} \underbrace{\sum_{i=1}^{N} \left(Y_i - h(\mathbf{X}_i; \theta)\right)^2}_{\text{residual sum of squares, RSS}}$$

This is basically just [[Empirical risk minimisation]], as dividing RSS by $N$ under squares loss is exactly $E_{in}(h)$


# linear regression 

The basic model is a hyperplane in the features,

$$Y = \theta_0 + \theta_1 X_1 + \cdots + \theta_d X_d + \varepsilon$$

but the name is misleading, because the model extends immediately to

$$Y = \theta_0 \phi_0(\mathbf{X}) + \theta_1 \phi_1(\mathbf{X}) + \cdots + \theta_k \phi_k(\mathbf{X}) + \varepsilon$$

where the **[[basis]] functions** $\phi_j$ can be anything at all: powers, logarithms, sines, indicator functions, products of variables. 



# [[nonparametric methods|Nonparametric]] regression 

We drop the parametric family and estimate $f^*(\mathbf{x})$= $\mathbb{E}(Y|\mathbf{X}=\mathbf{x})$ by average $Y_{i}$ of the observations near $\mathbf{x}$

### ![[Nadaraya–Watson kernel regression]]


