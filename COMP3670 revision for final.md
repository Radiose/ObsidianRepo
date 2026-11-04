Target functions:
The rule with the smallest out of sample error
$f^*(\mathbf{x})=\eta(\mathbf{x})=\mathbb{E}(Y|\mathbf{X}=\mathbf{x})$
$f^*(\mathbf{x})=arg \ \max p_{y|\mathbf{x}}(y|\mathbf{x})$ - classification - given an $\mathbf{x}$, return what is most likely. 

Loss: $l((\mathbf{x},y)h)=\mathbb{1}\{ h(\mathbf{x})\not=y \}$ - binary 
				$= (y-h(\mathbf{x}))^2$

out of sample Errors 
Targets:
squared loss:  $L(f^*)=\mathbb{E}(var(Y|x))$ 
classification: $L(f^*)=\mathbb{E}[\min\{ \eta(\mathbf{X}),1-\eta(\mathbf{X}) \}]$ where $\eta(\mathbf{X})=\mathbb{E}(Y|\mathbf{X}=\mathbf{x})$ 
Classification - the error is the chance that it is wrong. If $\mathbb{P}(y=1|X=0)=0.1$, then it will be wrong 10% of the time. 


Chosen 
With the **squared loss**, $L(h) = \mathbb{E}[(h(\mathbf{X}) - Y)^2]$
With the **binary loss**, $L(h) = \mathbb{E}[\mathbb{1}\{h(\mathbf{X}) \neq Y\}] = \mathbb{P}(h(\mathbf{X}) \neq Y)$ - the chance its wrong



In vs out of sample error 
In sample:
$E_{in}(h)=\frac{1}{N}\sum(\ell(\mathbf{X}_{i},Y_{i}),h)$
Out of sample 
$\mathbb{E}[\ell((\mathbf{X}_{i},Y_{i}),h])$




Generalisation gap:
The difference between the two 

Hoeffdings:
For $W_{1},\dots,W_{n}$ IID random variables taking values in $[0,1]$, with $\mathbb{E}[W_{i}]=\mu$, then $\forall \epsilon>0$
$\mathbb{P}\left( \left\lvert   \frac{1}{N}\sum_{i=1}^N W_{i}-\mu  \right\rvert>\epsilon \right) \leq 2e^{-2N\epsilon^{2}}$
The sample average tends to the expected value with $N$
creating the generalised bound 
$\mathbb{P}(\lvert E_{in}-E_{out} \rvert>\epsilon)\leq 2e^{-2N\epsilon^2}$

### verification vs learning 
Fixing $h$ before looking at the sample is verification.
Union bound 
for $M$ hypotheses:
$\mathbb{P}(max_{h \in \mathcal{H}} |E_{out}-E_{in}|>\epsilon)<2Me^{-2N\epsilon^2}$

So for fixed $h$, 
$E_{in}(h)\leq E_{out}(h) + \sqrt{ \frac{1}{2N}\log\left( \frac{2}{\delta} \right) }$
Error decreases in $\frac{1}{\sqrt{ N }}$

Important: 
$$E_{out}(\hat{h}_{n})-E_{out}(f^*)=(E_{out}(h^*)-E_{out}(f^*))+(E_{out}(\hat{h}_{N})-E_{out}(h^*))$$
total error is approximation + estimation error 


Simple random sample : IID 


Parametric method: 

Normal $\theta=(\mu,\sigma^2)$

Maximum likelihood estimator 
$\mathcal{L}(\theta)= \prod_{i=1}^N p(z_{i}|\theta)$
where $Z_{1},\dots,Z_{n}$ is a random sample.


Logit:
$\eta(\mathbf{x}|\mathbf{\theta})=\frac{1}{1+e^{-\left( \sum_{j=1}^d w_{j}x_{j}+w_{0} \right)}}$

Cross entropy loss:
For h with codomain $(0,1)$
$\ell((\mathbf{x},y),\eta)=-y\log(\eta(\mathbf{x})-(1-y)\log(1-\eta(\mathbf{x}))$

Note that $\hat{\theta}=arg\ \max_{\theta}(LL(\theta))=arg\ \min \frac{1}{N} \sum_{i=1}^N \ell((\mathbf{X}_{i},Y_{i}),\eta(\cdot|\mathbf{\theta}))$
cross entropy - scores probabilities not just right or wrong



![[Pasted image 20261102161807.png|368]]

Kernel ![[Pasted image 20261102161558.png]]


SVM 
Hard:
minimize $\frac{1}{2}\lVert \mathbf{w} \rVert_{2}^2$
	subject to $y_{i}(\langle \mathbf{w},\mathbf{x}_{i} \rangle+b)\geq 1\quad (i=1,\dots,n)$

Soft:
Minimise 



OUTER PRODUCT 
any matrix of rank 1 can be written as an outer product $vv^T$

PCA
For a covariance matrix $\mathbf{C}$
$\mathbf{q}_{1},\dots,\mathbf{q}_{n}$ are its orthonormal eigenbasis with $\lambda_{1},\dots \lambda_{n}$ eigenvalues(decreasing)
$Q_{k} \in \mathbb{R}^{d \times k}$ is the matrix of its orthonormal eigenbasis 
$z_{i}=Q^T_{k}(\mathbf{x}_{i}-\mu) \in \mathbb{R}^k$
$Z=X_{C}Q_{k}\in \mathbb{R}^{n \times k}$
whos $i$th row is $\mathbf{z}^T_{i}$
$S_{k}=span\{ q_{1},\dots,q_{k} \}$
$z_{i}$ gives coordinates of its projection onto $S_{k}$

Reconstruction of $\mathbf{x_{i}}$
$\hat{\mathbf{x}}_{i}=\mu+UU^T(\mathbf{x}_{i}-\mu)$
Average squared reconstruction error 
$E(U)= \frac{1}{n}\sum_{i=1}^n \lVert \mathbf{x}_{i}-\mathbf{\hat{x}}_{i} \rVert_{2}^2 \geq \sum_{\ell = k+1}^{d}\lambda_{\ell}$ - the eigenvalues of $C$ excluded

When $\mathbf{U}=\mathbf{Q}_{k}$, equality is obtained 

Explained variance ratio $\rho_{k}= \frac{\sum_{j=1}^{k}\lambda_{j}}{\sum_{j=1}^{d}\lambda_{j}}$


SVD:
Given some matrix $A$
SV are square roots of eigenvalues of $A^TA$
SVD form $U \sum V^T$
where $\mathbf{v}_{1},\dots,\mathbf{v}_{n}$ are the orthonormal eigenvectors of $A^TA$ and form the columns of $V$
And the columns of $U$ are $\mathbf{u}_{1}= \frac{A\mathbf{v}_{1}}{\sigma_{1}}$ where $\sigma$ are the singular values of $A^TA$
Truncated:
$A_{r}=\sum_{i=1}^r \sigma_{i}\mathbf{u}_{i}\mathbf{v}_{i}^T=U_{k}\sum_{k}V_{k}^T$
For rank $B$
Error: $\lVert A-B \rVert_{F}^2 \geq \lVert A -A_{k} \rVert_{F}^2 = \sum_{i=k+1}^r \sigma_{i}^2$
The sum of eigenvalues is the error 
Storing the three truncated gives $k(m+d+1)$ - saving only when k is small 


logistic function derivative 
$\sigma'(z)=\sigma(z)(1-\sigma(z))$


Hessian:
matrix of second partial derivatives. 
$H_{j,k}= \frac{ \partial ^2 f }{ \partial x_{j}\partial x_{k} }$ - well behaved functions have positive semidefinite hessians 
If all eigenvalues of hessian are non negative, then convex 

Least squares, ridge + logistic regression, soft margin SVM are all convex 
LS matrix:
$Y=\theta_{0} \phi_{0}(X)+\dots+\theta_{k}\phi_{k}(X)+\epsilon$
Stacking $Y= (y_{1},\dots,y_{n})^T$, $X=\begin{bmatrix}\phi_{0}(X_{1}) & . & . & . & \phi_{k}({X}_{1})  \\ .  \\ .   \\ .   \\  \phi_{0}({X_{n}}) & . & . & . &\phi_{k}({X_{n}}) \end{bmatrix}$
RSS($\theta$)=$\lVert \mathbf{Y}-\mathbf{X}\mathbf{\theta} \rVert^2$
Row $i$ of $X\theta$ is the prediction for observation $i$.
$\nabla RSS(\theta)=-2X^T(\mathbf{Y}-X\theta)$



Gram schmidt 
For a basis $v_{1},\dots,v_{n}$ of $V$
$e_{1}=\frac{v_{1}}{\lVert  v_{1} \rVert}$
$e_{j}= \frac{v_{j}- \langle v_{j}-e_{1} \rangle e_{1}-\dots-v_{j}-\langle v_{j}-e_{j-1} \rangle e_{j-1}}{\lVert v_{j}- \langle v_{j}-e_{1} \rangle e_{1}-\dots-v_{j}-\langle v_{j}-e_{j-1} \rangle e_{j-1} \rVert}$
