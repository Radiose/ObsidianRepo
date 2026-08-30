# Definition 
an eigenvector with eigenvalue $\lambda$ is a non-zero vector $v \in V \setminus \{ \mathbf{0} \}$ such that $T \mathbf{v}=\lambda \mathbf{v}$ where $\lambda$ is the corresponding [[eigenvalue]]


# Theorem 1
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


# Corollary 
Suppose $V$ is finite dimensional 
Then, any $T \in \mathcal{L}(V)$ has at most $\dim(V)$ distinct [[eigenvalue]]s

This is because every eigenvalue gives you some eigenvector, and for distinct eigenvalues, they are linearly independent, and thus the dimension of a linearly independent set is at most the dimension of the vector space 


# Theorem 2
Suppose that $\lambda_{1}\dots \lambda_{m}$ are distinct eigenvalues of $T$. 

Then 
i) The sum of eigenspaces is a [[internal direct sum of subspaces|direct sum]] ($E(\lambda;T) \oplus\dots \oplus E(\lambda_{m};T)$ is direct)
ii) if $V$ is finite dimensional, $\sum_{i=1}^m(\dim(E(\lambda_{1};T_{1}))\leq \dim(V)$
### Proof 
ii) follows from i) because [[internal direct sum of subspaces|direct sum]] is a subspace
IE $\sum\dim(E(\lambda_{i};T))=\dim(E(\lambda_{1};T))\oplus\dots \oplus \dim(E(\lambda_{m};T)) \leq \dim(V)$ 
The proof of i) will need a bit more work 
i)
suppose $\mathbf{u}_{i} \in E(\lambda_{i};T)$ s.t $\mathbf{u_{1}}+\dots+\mathbf{u}_{m}=\mathbf{0}$
Assume not all $\mathbf{u}_{i}=\mathbf{0}$
Pick the non zero $\mathbf{u}_{i}$, so $\mathbf{u}_{i_{1}},\dots,\mathbf{u}_{i_{k}} = \mathbf{0}$
Then, $\{ \mathbf{u}_{i_{1}},\dots,\mathbf{u_{i_{k}}} \}$ are [[linearly independent]]
But via [[eigenvector#Theorem 1|theorem 1]], $\{ \mathbf{u}_{i_{1}},\dots,\mathbf{u_{i_{k}}} \}$ are linearly independent. 
Thus, $\mathbf{u}_{i}=\mathbf{0}\quad \forall i \in \{ 1\dots m \}$


