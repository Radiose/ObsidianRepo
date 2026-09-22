Decision trees:


ERM
Risk: $\quad L(h) = \mathbb{E}\big[\ell((\mathbf{X}, Y), h)\big] = \int \ell((\mathbf{x}, y), h)\, dP(\mathbf{x}, y)$ = out of sample error 
Empirical risk: $L_{\mathcal{D_{n}}}(h)=\frac{1}{N}\sum_{i=1}^N \ell((\mathbf{X_{i},}Y_{i}),h)$

Hoeffdings: 
$E_{out }(h)\leq E_{in}(h)+\sqrt{ \frac{1}{2N}\log \frac{2}{\delta} }$ for a fixed h
For a set of h: 
$E_{out }(h)\leq E_{in}(h)+\sqrt{ \frac{1}{2N}\log \frac{2M}{\delta} }$ - where m is the quantity of hypotheses in $\mathcal{H}$

Fundamental theorem of statistical learning
[[Empirical risk minimisation]] on some $\mathcal{H}$ is consistent for every distribution $P \iff d_{VC}(\mathcal{H})<\infty$.
Consistent means: $E_{out}(\hat{h}_{N}) \to E_{out}(h^*)$ as $N \to \infty$, with probability 1 over all possible samples. 
(Basically, the idea is that with enough data, we can falsify all hypothesis).


[[Shatter coefficient]]
$2^N$ dichotomies for $N$ points. 
$S(\mathcal{H},N)$, the shatter coefficient, is the number of distinct dichotomies that $\mathcal{H}$ can produce on $N$ points. 
If $S(\mathcal{H},N)\leq{2}^N$ $\mathcal{H}$ shatters $N$ points. 
VC DIM $d_{VC}(\mathcal{H})$- number of points that H can shatter. - worst case 
vc bound: $E_{out}(h)\leq E_{in}(h)+\sqrt{ \frac{32}{N}\left[ v\log(N+1)+\log \frac{8}{\delta} \right] }$ - useful for infinite size $\left| \mathcal{H} \right|$ - importantly tends to 0 as $N$ goes to infinity






To show $d_{VC}\geq k$, exhibit one set of $k$ points labelled in all $2^k$ ways. 
to show $d_{VC}<k+1$, show that no set of $k+1$ points can be labelled in all ways. 

# squared loss 
For continuous cases, we use the squared loss 
$l(\mathbf{x},y)h)=(y-h(\mathbf{x}))^2$

For discrete, we can use the binary loss 
$l((\mathbf{x},y)h)=\mathbb{1}\{ h(\mathbf{x})\not=y \}$


$\text{VAR} [X]=E[X^2]-(E[X])^2$



PLUGIN RULES 
Goal: $\hat{h}(\mathbf{x})=\mathbb{1}\left\{  \hat{\eta}(\mathbf{x})> \frac{1}{2}  \right\}$
$\eta(\mathbf{x})=\mathbb{P}(Y=1|X=\mathbf{x})$

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
The logit is a weighted score of the features, with $\theta=(w_{0},\dots,w_{n})$
We then apply this to the idea of $\eta(\mathbf{x})=\mathbb{P}(Y=1|X=\mathbf{x})$
$\log \frac{\eta(\mathbf{x}|\theta)}{1-\eta(\mathbf{x}|\theta)}=\sum_{j=1}^d w_{j}x_{j}+w_{0}\iff \eta(\mathbf{x}|\theta)=\frac{1}{1+e^{-\left( \sum_{j=1}^d w_{j}x_{j}+w_{0}\right)}}$ 
![[Pasted image 20260920125741.png]]
The idea is that using $\eta(\mathbf{x})$, we want to minimise our cross entropy loss 
Cross entropy loss:

$\ell((\mathbf{x},y),\eta)=-y\log(\eta(\mathbf{x})-(1-y))\log(1-\eta(\mathbf{x}))$
Getting the maximum likelihood $\theta$ is just running ERM with cross entropy loss 
$\hat{\theta}=arg_{\theta}max(LL(\theta))=arg_{\theta}min \frac{1}{N}\sum_{i=1}^N \ell((\mathbf{X_{i},Y_{i}}),\eta(.|\theta))$
The weights such that the loss is the minimum over all $x_{i}$

This is derived from 
$LL(\theta)=\log(\mathcal{L}(\theta))=\sum_{i=1}^N \left[ Y_{i}\log \eta(\mathbf{X_{i}|\theta})+(1-Y_{i})\log(1-\eta(\mathbf{X_{i}|\theta})) \right]$
(for bernoulli)
Maximising LL is the same as minimising $-\frac{LL}{N}$ - average of sample of loss.
So obviously, the hypothesis set is the set of non zero weights summed together, which is the perceptron. 



NONPARAMETRIC CLASSIFICATION:
$\kappa$ is the shape of the bump, $\sigma$ is the width - the smoothing parameter. 
$W_{i}(\mathbf{x})=\frac{\kappa\left( \frac{\mathbf{x}-\mathbf{X_{i}}}{\sigma} \right)}{\sum_{j=1}^N \kappa\left( \left( \frac{\mathbf{x-\mathbf{X}}_{j}}{\sigma} \right) \right)}$
$\kappa$ can look like for example $\kappa(u)=\frac{1}{\sqrt{ 2\pi }}e^{-u^2/2}$
General rule  for NP plugin
$\hat{\eta}(\mathbf{x})=\sum_{i=1}^N W_{i}(\mathbf{x})\mathbb{1}\{ Y_{i}=1 \}$


DECISION TREE 
Impurity satisfies:
Region with one class is pure 
Region split 50/50 is inpure 
increases up to $\frac{1}{2}$ and decreases from $\frac{1}{2}$
Three choices:
entropy $-p\log p-(1-p)\log(1-p)$
gini: $2p(1-p)$
misclassification: $min(p,1-p)$
Where $p$ is the proportion of points in class $1$ (for binary)
Misclassification is the error of the best possible classifier $f^*$
Impurity drop:
$\Delta_{R}(j,\alpha)=I(R)- \frac{N(R^j_{\alpha,^-})}{N(R)}I(R_{\alpha,^-}^j) - \frac{N(R_{\alpha,^+}^j)}{N(R)}I(R_{\alpha,^+}^j)$

$I(R)$ = original impurity - $R_{\alpha^-}^j$, $R_{\alpha^+}^j$ - two regions split at $\alpha$ threshold. $N(R)$ - count of elements in region R. 
At each step of the tree, we want to maximise $\Delta_{r}$ out of all possible $j,\alpha$


REGRESSION 
PARAMETRIC:$$
\hat{\theta} = \operatorname*{arg\,min}_{\theta \in \Theta} \underbrace{\sum_{i=1}^{N} \left(Y_i - h(\mathbf{X}_i; \theta)\right)^2}_{\text{residual sum of squares, RSS}}$$
basically ERM 

LINEAR REGRESSION:
The model is a hyperplane in the features 
$Y=\theta_{0}+\theta_{1}X_{1}+\theta_{2}X_{2}+\dots+\theta_{d}X_{d}+\epsilon$
But, its not exactly *linear*, model extends immediately to 
$Y=\theta_{0}\phi_{0}(\mathbf{X})+\dots+\theta_{1}\phi_{1}(\mathbf{X)}+\epsilon$
The important part is that the linear dependence is on $\theta$. 

NONPARA 
Nadaraya Watson kernel regression 
$\sum_{i=1}^N W_{i}(\mathbf{x})Y_{i}$
$W_{i}$ is exactly the same for kernel classification 




[[Simpson's rule]]
[[Trapezoidal rule]]
