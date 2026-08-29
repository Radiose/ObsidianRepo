Given a [[vector subspace|subspace]] $u \subseteq V$, we say its annihilator is the [[subset]] of $V^V$ (the [[dual vector space]]) such that $Ann(U)=\{ \phi \in V^V |U \subseteq ker(\phi)\}$

## Remark
$Ann(U)$ is a [[vector subspace|subspace]]
### Proof 

We use [[vector subspace#Theorem|subspace theorem]]
i) $\mathbf{0}\in Ann(U)$

ii) Let $\phi, \gamma \in Ann(u)$. Take $\mathbf{u}\in U$, then $(\gamma+\phi)(\mathbf{u})=\phi(\mathbf{u})+\gamma(\mathbf{u})=\mathbf{0}+\mathbf{0}$
$\implies U \in \ker(\phi+\gamma)$
A similar proof applies to iii) 


# Theorem 1
If $V$ is [[finite dimensional]], $U$ is a [[vector subspace|subspace]], then $\dim(U)+\dim(ann(U))=\dim(V)$
### Proof 
Let $\{ \mathbf{u_{1}},\dots,\mathbf{u}_{k} \}$ be a [[basis]] of $U$
Via [[basis#Theorem 2 (linear independent list extends to a basis)|this theorem]], we extend to a basis of $V = \{ \mathbf{u_{1}},\dots,\mathbf{u_{k}},\dots,\mathbf{u}_{n} \}$
Consider the [[Dual basis]] $\{ \phi_{1},\dots,\phi_{n} \}$ of $V^V$
We claim that $ann(U)=span\{ \phi_{k+1},..,\phi_{n} \}$ of $V^V$
$\forall i>k,\phi_{i}(\mathbf{u_{j}})=0$ when $j \leq k$
$\implies U \in \ker(\phi _{i})$
$\implies \phi_{i} \in ann(U)$
$\implies \dim(ann(U))\geq n-k$
On the other hand, $ann(u) \oplus Span(\phi_{1},\dots,\phi_{k})$ is a [[internal direct sum of subspaces|direct sum]]
$\implies \dim(ann(U))+k \leq \dim(V^V)=n$
COME BACK 