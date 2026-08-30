---
aliases:
  - nilpotent
---
# Motivation
If we have $V=G(\lambda_{1},T)\oplus\dots \oplus G(\lambda_{m},T)$
#### Observe 
Pick $U = G(\lambda_{i},T)$ for some $i$
Then, $U=G(0,T-\lambda_{i})$
If also $\dim(U)<\infty$, then $N:=(T-\lambda)|_{u}$ is such that $N^{\dim(U)}=\mathbf{0}$ the zero [[linear operator|operator]]

# Definition 
An [[linear operator|operator]] $N$ is *nilpotent* if $\exists d>0$ such that $N^d=0$


For example, $\begin{bmatrix}0 &  1 \\  0 & 0\end{bmatrix}$ is a [[nilpotent operator]] on $\mathbb{F}^2$


# Theorem 
If $U$ is [[finite dimensional]] and $N \in \mathcal{L}(U)$ is nilpotent, then $\exists$ some basis $B$ of $U$ such that 
$[N]_{B}=$
![[Pasted image 20260830160233.png|212]]


### Proof 
1: 
If $U$ is non zero, then pick the largest $i_{1}>0$ such that $N^{i_{1}}\not=0$,
then $\exists \mathbf{u_{1}}\in U$ such that $N^{i_{1}} (\mathbf{u_{1}})\not=\mathbf{0}$ 
2:
$B_{1}=\{ N^{i_{1}}u_{1},N^{i_{1}-1}\mathbf{u}_{1},\dots,N \mathbf{u}_{1},\mathbf{u_{1}} \}$
Claim: $B_{1}$ is [[linearly independent]]
Pick some linear combination $c_{i_{1}}N^{i_{1}}$