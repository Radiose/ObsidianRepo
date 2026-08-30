---
aliases:
  - generalised eigenvector
---
# definition
The generalised [[eigenspace]] $G(\lambda,T)$ is defined as following
$G(\lambda,T):=\bigcup_{m>0} \ker((T-\lambda id)^m)$

where $v\in G(\lambda,T) \setminus \{ \mathbf{0} \}$ is a generalised [[eigenvector]] with eigenvalue $\lambda$

# example 
Recall the derivation linear transformation 
$D:\mathbb{F}[x]\to \mathbb{F}[x]$, $D(x^n)=nx^{n-1}$
its eigenspace, $E(0,D)=Span\{ 1 \}$
Its generalised eigenspace, $G(0,D)=\mathbb{F}[x]$ or the entire [[vector space]]
This is because if we differentiate everything enough we get to $0$


The reason we want to talk about generalised eigenspaces is because it will allow us to decompose our operator $T$ into smaller blocks 

# Theorem 
If $\lambda_{1},\dots,\lambda_{m}$ are distinct, generalised [[eigenvalue]]s of $T$, then $G(\lambda_{1},T)+\dots+G(\lambda_{m},T)$ is a [[(external) direct sum of vector spaces|direct sum]].
Additionally, if $V$ is [[finite dimensional]], then $\dim(G(\lambda_{1},T))+\dots+\dim(G(\lambda_{m},T))\leq \dim(V)$

### Proof 
The second claim follows from the first, as the dimension of [[vector subspace|subspace]]s are additive with respect to their direct sum. The dimension of a subspace is at most the dimension of the ambient space $V$.

Assume that $\mathbf{u}_{i}\in G(\lambda_{i},T)$ such that $\mathbf{u_{1}}+\dots+\mathbf{u_{m}}=0$. 
We need to show that $\mathbf{u_{1}}=\dots=\mathbf{u}_{m}=0$
After possible reordering, we arrange $\mathbf{u_{1}}+\dots+\mathbf{u_{k}}=0$ and $\mathbf{u_{k+1}}=\dots=\mathbf{u}_{m}=0$
where $k \leq m$.

We want to pick a sum with minimal possible $k$

#### Case: $k>0$
$\exists d_{k}\in \mathbb{N}$ such that $(T-\lambda \cdot id)^{dk}\mathbf{u}_{k}=\mathbf{0}$
Apply $(T-\lambda_{k}\cdot id)^{d_{k}}$  to $\mathbf{u_{1}}+\dots+\mathbf{u_{k}}$
$(T-\lambda_{k}\cdot id)\mathbf{u}_{1}+\dots+(T-\lambda_{k}\cdot id)\mathbf{u_{k-1}}+\mathbf{0}=\mathbf{0}$
##### Observe
Each $G(\lambda _{i},T)$ is [[invariant subspace|invariant]] under $T$, because $(T-\lambda_{i}\cdot id)(\mathbf{u_{i}})\in G(\lambda_{i},T)$ 
and $T(\mathbf{u}_{i})=(T-\lambda_{i},id)(\mathbf{u_{i}})+\lambda_{i}\mathbf{u_{i}}$
Similarly $G(\lambda_{i},T)$ is [[invariant subspace|invariant]] under $T-\lambda_{k}id$ (via the rewriting of $T(\mathbf{u}_{i})$ above)

Thus, $(T-\lambda_{k}\cdot id)\mathbf{u}_{1}+\dots+(T-\lambda_{k}\cdot id)\mathbf{u_{k-1}}+\mathbf{0}=\mathbf{0}$ has each $(T-\lambda _{k}id)\mathbf{u_{i}} \in G(\lambda_{1},T)\setminus \{ \mathbf{0} \}$
This contradicts the minimality, as we have $k-1$ nonzero terms. The key bit is that vectors after being applied by $(T-\lambda _{k} \cdot id)^{dk}$ are still in the original vector space so we have a contradiction. 



