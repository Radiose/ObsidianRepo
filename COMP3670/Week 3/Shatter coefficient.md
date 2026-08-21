Consider the case of binary classification. Fix $N$ points, $\mathbf{x_{1}},\mathbf{x_{2}},\dots,\mathbf{x_{n}}$. Each hypothesis $h \in \mathcal{H}$ produces a [[sequence]] of labels. Such a sequence is called a **dichotomy.**

There are at most $2^N$ dichotomies in total. The effective number of hypothesis is not $|\mathcal{H}|$, but in fact the number of distinct dichotomies that $\mathcal{H}$ can actually produce. 

The shatter coefficient $S(\mathcal{H},N)$ is the largest number of distinct dichotomies that the hypothesis in $\mathcal{H}$ can produce on $N$ points, where we are free to place the $N$ points wherever is most favourable.
## Properties 
$S(\mathcal{H},N)\leq {2}^N$, since there are only $2^N$ label sequences in total. 
when $S(\mathcal{H},N)\leq {2}^N$, we say that $\mathcal{H}$ **shatters** $N$ points. 

![[Vapnik-Chervonenkis dimension]] 
