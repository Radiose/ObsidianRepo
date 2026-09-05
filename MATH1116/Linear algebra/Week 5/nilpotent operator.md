---
aliases:
  - nilpotent
---
# Motivation
If we have $V=G(\lambda_{1},T)\oplus\dots \oplus G(\lambda_{m},T)$
#### Observe 
Pick $U = G(\lambda_{i},T)$ for some $i$
Then, $U=G(0,T-\lambda_{i})$
If also $\dim(U)<\infty$, then $N:=(T-\lambda)|_{u}$ is such that $N^{\dim(U)}=\mathbf{0}$ = the zero [[linear operator|operator]]

# Definition 
An [[linear operator|operator]] $N$ is *nilpotent* if $\exists d>0$ such that $N^d=0$


For example, $\begin{bmatrix}0 &  1 \\  0 & 0\end{bmatrix}$ is a [[nilpotent operator]] on $\mathbb{F}^2$


# Theorem 
If $U$ is [[finite dimensional]] and $N \in \mathcal{L}(U)$ is nilpotent. Then, there exists some set of linearly independent vectors $\{ \mathbf{u}_{1},\dots,\mathbf{u}_{k} \}$ and a [[sequence]] of non-negative integers $i_{1}\geq\dots\geq i_{k}\geq {0}$ such that the set 
$$\{ N^{i_{1}}(\mathbf{u_{1}}),\dots,N(\mathbf{u}_{1}),\mathbf{u}_{1},
\dots N^{i_{k}}(\mathbf{u}_{k}),\dots,N{\mathbf{u}_{k}} \}$$
is a basis of $U$. In this basis, the matrix of $N$ is as follows:

![[Pasted image 20260830160233.png|496]]


### Proof 
1: 
If $U$ is non zero, then pick the largest $i_{1}>0$ such that $N^{i_{1}}\not=0$,
then $\exists \mathbf{u_{1}}\in U$ such that $N^{i_{1}} (\mathbf{u_{1}})\not=\mathbf{0}$ 

2:
$B_{1}=\{ N^{i_{1}}u_{1},N^{i_{1}-1}\mathbf{u}_{1},\dots,N \mathbf{u}_{1},\mathbf{u_{1}} \}$
Claim: $B_{1}$ is [[linearly independent]]
Pick some linear combination $c_{i_{1}}N^{i_{1}}\mathbf{u_{1}}+\dots+c_{1}N\mathbf{u}_{1}+c_{0}\mathbf{u}_{1}=0$
Apply $N^{i_{1}}$
$\mathbf{0}+\dots+\mathbf{0}+c_{0}N^{i_{1}}\mathbf{u}_{1}=\mathbf{0}$
$\implies c_{0}=0$
Apply $N^{u_{1}-1}$ gives us $\mathbf{0}+\dots+\mathbf{0}+c_{1}N^{i_{1}}\mathbf{u}_{1}+0N^{i_{1}-1}\mathbf{u_{1}}=\mathbf{0}$
$\implies c_{1}=0$
Applying on and on gives $c_{i_{1}}=\dots=c_{1}=c_{0}=0$

3:
$U_{1}:=Span(B_{1})$ which is an [[invariant subspace|invariant]] under $N$. This is literally from the definition of $B_{1}$ in (2:)
The goal of the third step is to provide a candidate vector space such that it is complement to $U_{1}$, but also invariant. 

Since $N^{i_{1}}\mathbf{u_{1}}\not=\mathbf{0}$, we can pick up $\phi:U\to \mathbb{F}$ such that $\phi(N^{i_{1}}\mathbf{u_{1}})\not=0$
Define $S:U \to \mathbb{F}^{i_{1}+1}$, $S(\mathbf{v})=\begin{bmatrix}\phi(\mathbf{v}) \\  \phi(N\mathbf{v}) \\  . \\  . \\  . \\ \phi(N^{i_{1}}\mathbf{v}) \end{bmatrix}$
Define $W_{1}:=\ker(S)$

Claim:
$W_{1}:=\ker(S)$ is [[invariant subspace|invariant]] under $N$. 
if $\mathbf{v}\in W_{1}$, consider 
$S(N \mathbf{v})=\begin{bmatrix} \phi(N\mathbf{v}) \\  . \\  . \\  \phi(N^{i_{1}}\mathbf{v})  \\  \phi(N^{i_{1}+1}\mathbf{v})\end{bmatrix}$
All the terms up until the last $=0$, as $\mathbf{v}\in W_{1}$
The last term $N^{i_{1}+1}$ is the zero operator, and because $\phi$ is linear, it must $=0$

4: 
Prove $W_{1}+U_{1}$ is a [[internal direct sum of subspaces|direct sum]]
We show $U_{1} \cap W_{1}=\{ \mathbf{0} \}$
