We want the target function $f^*$, which has the smallest out of sample error. 
We cannot have this, because the out of sample error is impossible to know in most cases, as the distribution $P$ is not known. 

What we can do is compute the in sample error, which we do by the following 
**risk** (out-of-sample error): $\quad L(h) = \mathbb{E}\big[\ell((\mathbf{X}, Y), h)\big] = \int \ell((\mathbf{x}, y), h)\, dP(\mathbf{x}, y)$

$L_{\mathcal{D_{n}}}(h)=\frac{1}{N}\sum_{i=1}^N \ell((\mathbf{X_{i},}Y_{i}),h)$
We estimate some minimiser of $L$ by a minimiser of $L_{\mathcal{D}_{n}}$.

statistical learning framework:

![[generalisation gap]]

The goal is to control $$\mathbb{P}(max_{h \in \mathcal{H}}|E_{out}-E_{in}|>\epsilon)\leq\delta$$

Read as: the probability with at least $1-\delta$, no hypothesis in $\mathcal{H}$ has a gap larger than $\epsilon$ and in particular, 
$E_{out}(\hat{h_{N}})\leq E_{in}(\hat{h_{N}})+\epsilon$

$\epsilon$ is how wrong we may be, and $\delta$ is how often that may occur. Both must be controlled by the things we can choose. Sample size $N$, and [[hypothesis set]] $\mathcal{H}$.

We still cannot prove that some rule fitted on a finite sample will work on new data, but what we can do is bound the probability of being wrong, and by how much. 


# The overarching idea 
We start off with a prechosen hypothesis set, and our goal is to compute $E_{in}(h)$ for each $h \in \mathcal{H}$. We aim then to return the $h$ that has the lowest in sample error. 