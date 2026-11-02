Target functions:
The rule with the smallest out of sample error
$f^*(\mathbf{x})=\eta(\mathbf{x})=\mathbb{E}(Y|\mathbf{X}=\mathbf{x})$
$f^*(\mathbf{x})=arg \ \max p_{y|\mathbf{x}}(y|\mathbf{x})$ - classification - given an $\mathbf{x}$, return what is most likely. 

Errors:
squared loss:  $L(f^*)=\mathbb{E}(var(Y|x))$ 
classification: $L(f^*)=\mathbb{E}[\min\{ \eta(\mathbf{X}),1-\eta(\mathbf{X}) \}]$ where $\eta(\mathbf{X})=\mathbb{E}(Y|\mathbf{X}=\mathbf{x})$ 
Classification - the error is the chance that it is wrong. If $\mathbb{P}(y=1|X=0)=0.1$, then it will be wrong 10% of the time. 


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




OUTER PRODUCT 
any matrix of rank 1 can be written as an outer product $vv^T$

PCA 
