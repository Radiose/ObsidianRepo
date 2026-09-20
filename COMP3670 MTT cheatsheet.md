Decision trees:


ERM
# squared loss 
For continuous cases, we use the squared loss 
$l(\mathbf{x},y)h)=(y-h(\mathbf{x}))^2$

For discrete, we can use the binary loss 
$l((\mathbf{x},y)h)=\mathbb{1}\{ h(\mathbf{x})\not=y \}$


$\text{VAR} [X]=E[X^2]-(E[X])^2$



PLUGIN RULES 

Parametric:
Classification
Assume shape, (bernoulli, normal distr). Estimate parameters, ($\theta$, $\sigma$) 
Likelihood function:
For IID sample $Z_{1},\dots,Z_{n}$, $\mathcal{L}(\theta)=\prod_{i=1}^N p(Z_{i}|\theta)$
(independence allows this)
Bernoulli $\theta$: $\frac{k}{N}$
Normal: $\frac{1}{N}\sum Z_{i}$ for $\hat{\mu}$, $\hat{\sigma}^2=\frac{1}{N}\sum(Z_{i}-\hat{\mu})^2$

Note that if the family is wrong, $\hat{\theta}$ will converge to the $\theta$ closest to the truth, which may still not be anywhere near $\theta^*$

LOGIT:
$logit(p)=\log \frac{p}{1-p}$
We map a real number to a value between 0 and 1. 
The logit is a weighted score of the features, with $\theta=(w_{0})$
We then apply this to the idea of $\eta(\mathbf{x})=\mathbb{P}(Y=1|X=\mathbf{x})$
$\log \frac{\eta(\mathbf{x}|\theta)}{1-\eta(\mathbf{x}|\theta)}=\sum_{j=1}^d w_{j}x_{j}+w_{0}\iff \eta(\mathbf{x}|\theta)=\frac{1}{1+e^{-\left( \sum_{j=1}^d w_{j}x_{j}+w_{0}\right)}}$ 
