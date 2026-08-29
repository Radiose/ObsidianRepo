# Definition 
an eigenvector with eigenvalue $\lambda$ is a non-zero vector $v \in V \setminus \{ \mathbf{0} \}$ such that $T \mathbf{v}=\lambda \mathbf{v}$


# Theorem 
Let $T \in \mathcal{L}(V)$
Suppose $\{ \mathbf{v_{1}},\dots,\mathbf{v_{n}} \}\in V$ are [[eigenvector]]s of $T$, with **distinct** eigenvalues $\lambda_{1},\dots,\lambda_{k-1}$
Then, $\{ \mathbf{v_{1}},..,\mathbf{v_{n}} \}$ is [[linearly independent]]
### Proof 
Via contradiction, assume that $\{ \mathbf{v_{1}},\dots,\mathbf{v_{n}} \}$ is [[Linearly dependent]]
Then, via [[linear dependence lemma]], $\exists j \ s.t$ $\mathbf{v}_{j}\in span \{ \mathbf{v}_{1},\dots,\mathbf{v}_{j-1} \}$
importantly, $span \{ \mathbf{v}_{1},\dots,\mathbf{v}_{j-1} \}$ must be [[linearly independent]]
Note that $j \not=1$ because [[eigenvector]]s cannot $= \mathbf{0}$
Thus, $\mathbf{v_{j}}=a_{1}\mathbf{v_{1}}+\dots+a_{j-1}\mathbf{v}_{j-1}$ for some $a_{i}\in \mathbb{F}$
Applying $T$
$T(\mathbf{v_{j}})=T(a_{1}\mathbf{v_{1}}+\dots+ a_{j-1}\mathbf{v_{j-1}})$
Because $\{ \mathbf{v_{1}},\dots,\mathbf{v_{n}} \}$ are eigenvectors, 
$= \lambda \mathbf{v}_{j}=a_{1}\lambda_{1}\mathbf{v}_{1}+\dots+a_{j-1}\lambda_{j-1}\mathbf{v}_{j-1}$
Now the key step 
$\mathbf{0}=(a_{1}\lambda_{1}\mathbf{v}_{1}+\dots+a_{j-1}\lambda_{j-1}\mathbf{v}_{j-1})-\lambda_{j}(a_{1}\mathbf{v_{1}}+\dots+a_{j-1}\mathbf{v}_{j-1})$
$=a_{1}(\lambda_{1}-\lambda_{j})\mathbf{v_{1}}+\dots+a_{j-1}(\lambda_{j-1}-\lambda_{j})\mathbf{v_{j-1}}$
Since $\lambda_{i}\not=\lambda_{j}\quad \forall i<j$, not all coefficients are $0$
$\implies \{ \mathbf{v_{1}},\dots,\mathbf{v}_{j-1} \}$ is linearly independent 
But, via the dependence lemma, that set must be linearly independent.
Thus a contradiction. 
