---
aliases:
  - Reisz representation theorem
---
# Definition 
For $W,V$ being linear, finite dimensional inner product spaces

The adjoint of a linear map, $T:V\to W$ is a [[linear map|map]] $T^*:W\to V$ such that
$$\forall \mathbf{v}\in V\quad\forall\mathbf{w}\in W\ \ \langle T\mathbf{v},\mathbf{w} \rangle=\langle \mathbf{v},T^*\mathbf{w} \rangle$$
Exercise:
If $T^*$ exists, it is a linear map

# Theorem (Reisz representation theorem)
If $V$ is finite dimensional, then $\forall \phi \in V^V$, $\exists! \mathbf{v}\in V$ such that $\forall \mathbf{u}\in V$, $\phi(\mathbf{u})=\langle \mathbf{u},\mathbf{v} \rangle$

### Proof 
We establish that $\Phi_{V}:V\to V^V$ is an [[isomorphism]], so $\exists!\mathbf{w}\in V$ such that $\Phi_{V}(\mathbf{w})=\phi$
Then, $\phi=\Phi(\mathbf{w})=\langle \_{},\iota(\mathbf{w}) \rangle$. Because $\iota$ is bijective, and $\Phi$ is isomorphic, $\phi$ is unique. 

# Corollary 
If $V,W$ are finite dimensional, then $\forall T:V\to W$, its adjoint map exists, and is unique 

### Proof 
Consider the functional $\phi \in V^V$ such that $\phi (\mathbf{v})=\langle T\mathbf{v},\mathbf{w} \rangle$. $\phi$ can be shown to be a [[linear functional]].
Then $\exists !\mathbf{u}\in V$ such that $\phi=\langle \_{},\mathbf{u} \rangle$ such that $T^*\mathbf{w}=\mathbf{u}$. (via [[adjoint linear map#Theorem (Reisz representation theorem)|this theorem]]).
Other construction:
$T^*(\mathbf{w})=\Phi_{V}^{-1}(T^V(\Phi _{V}(\mathbf{w})))$

# Theorem 2 
If $\alpha,\beta$ are [[orthonormal vectors|orthonormal basis]] of $V$, and $W$, then $[T^*]_{\alpha \leftarrow \beta}=[T]_{\beta \leftarrow\alpha}$


# Theorem 3 (properties)
For $U,V$ [[inner product space]]s fin dim, then $\forall S,T \in \mathcal{L}(V,W)$
$(1): (S+T)^*=S^*+T^*$
$(2):(\lambda S)=\bar{\lambda}S^*$
$(3):S^{**}=S$
Note that these first three properties can be obtained by proving that $(\_{})^*$ is an [[conjugate linear involution]] map.

$(4):(id_{V})^*=id_{V}$
$(5):\forall T \in \mathcal{L}(V,W),\ \forall S\in \mathcal{L}(U,V),\quad (TS)^*=S^*T^*$

### Proof 
$(ii)$
for $\mathbf{v}\in V$, $\mathbf{w}\in W$, $\langle \mathbf{v},(\lambda S)^*\mathbf{w} \rangle=\langle \lambda S\mathbf{v},\mathbf{w} \rangle=\langle S\mathbf{v},\bar{\lambda}\mathbf{w} \rangle$
=$\langle \mathbf{v},S^*(\bar{\lambda}\mathbf{w}) \rangle=\langle \mathbf{v},\bar{\lambda}S^* \rangle$
And by [[adjoint linear map|Reisz representation theorem]], we have that $(\lambda S)=\bar{\lambda}S^*$
$(3)$
$\langle S^{**}\mathbf{v},\mathbf{w} \rangle=\overline{\langle \mathbf{w},S^{**}\mathbf{v} \rangle}=\overline{\langle S^*\mathbf{w} ,\mathbf{v}\rangle}$
$=\langle \mathbf{v},S^*\mathbf{w} \rangle=\langle S\mathbf{v},\mathbf{w} \rangle$
$\implies S^{**}=S$


# Theorem 4 (adjoints swap Ker, Range using perp)
For $T:V\to W$
$(1): \ker(T^*)=Range(T)^\perp$
$(2):Ker(T^*)^\perp=Range(T)$
$(3): Range(T^*)=\ker(T)^\perp$
$(4):Range(T^*)^\perp=\ker(T)$
