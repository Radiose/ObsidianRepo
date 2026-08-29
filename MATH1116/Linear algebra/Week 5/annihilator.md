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
On the other hand, $ann(U) \oplus Span(\phi_{1},\dots,\phi_{k})$ is a [[internal direct sum of subspaces|direct sum]]
$\implies \dim(ann(U))+k \leq \dim(V^V)=n \blacksquare$


# Theorem 2
$T:V\to W$ is a linear map, then 
i) $\ker(T^V)=Ann(Range(T))$
ii)$\dim(\ker(T^V))=\dim(\ker(T))+\dim(W)-\dim(V)$
iii)$\dim(Range(T^V))=\dim(Range(T))$
iv)$Range(T^V)=Ann(\ker(T))$

### Proof 
i) Pick $\phi \in W^V$ such that $T^V (\phi)=0$
$\subseteq$
$0=(\phi \circ T)(\mathbf{v})=\phi(T\mathbf{v})$
Thus, $\phi \in Ann(Range(T))$
This is because $T(\mathbf{v})\in Range(T)$
$\implies \phi(T(\mathbf{v})) =0$
$\supseteq$
Suppose $\phi \in Ann(Range(T))$
$\implies \phi(T(\mathbf{v}))=0\quad \forall \mathbf{v}\in V$
$\implies 0=\phi \circ T ( \mathbf{v})=T^V (\phi)$ 
which is the same as saying $\phi \in Ker(T^V)$

ii) 
$\dim(\ker(T^V))=\dim(Ann(Range(T)))$ via i)
$\implies \dim(\ker(T^V))=\dim(W)-\dim(Range(T))$
$\implies \dim(\ker(T^V))=\dim(W)-(\dim(V)-\dim(\ker(T)))$
$\implies \dim(\ker(T^V))=\dim(\ker(T))+\dim(W)-\dim(V)$
iii:
