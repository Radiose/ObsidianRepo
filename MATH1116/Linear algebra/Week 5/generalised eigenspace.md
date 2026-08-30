---
aliases:
  - generalised eigenvector
---
# definition
The generalised eigenspace $G(\lambda,T)$ is defined as following
$G(\lambda,T):=\bigcup_{m>0} \ker((T-\lambda id)^m)$

where $v\in G(\lambda,T) \setminus \{ \mathbf{0} \}$ is a generalised [[eigenvector]] with eigenvalue $\lambda$

# example 
Recall the derivation linear transformation 
$D:\mathbb{F}[x]\to \mathbb{F}[x]$, $D(x^n)=nx^{n-1}$
its eigenspace, $E(0,D)=Span\{ 1 \}$
Its generalised eigenspace, $G(0,D)=\mathbb{F}[x]$