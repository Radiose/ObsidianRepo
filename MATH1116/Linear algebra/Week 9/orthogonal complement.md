Recall that if $V$ is [[finite dimensional]], it has an [[orthonormal vectors|orthonormal basis]].

# Definition 
If $U$ is a [[vector subspace|subspace]], its orthogonal complement is denoted by $U^\perp$, and is a [[vector subspace|subspace]] such that $$U^\perp:=\{ \mathbf{v}\in V | \forall \mathbf{u} \in U \quad \langle \mathbf{u},\mathbf{v} \rangle=0 \}$$Exercise: show that $U^\perp$ is a subspace 

# Theorem 
if $U$ is [[finite dimensional]], then $V=U \oplus U^\perp$

### Proof 
$(1)$ $U + U^\perp=V$

let $\mathbf{v}\in V$, and $\{ \mathbf{e}_{1},\dots,\mathbf{e}_{n} \}$ be an [[orthonormal vectors|orthonormal basis]] of $V$
Define $\mathbf{u}=\langle \mathbf{v},\mathbf{e}_{1} \rangle\mathbf{e}_{1}+\dots+\langle v,\mathbf{e}_{m} \rangle\mathbf{e}_{m} \in U$
Define $\mathbf{w}:=\mathbf{v}-\mathbf{u}$ $\implies$$\mathbf{v}=\mathbf{u}+\mathbf{w}$
We can check that $\forall i \in \{ 1,\dots,m \} ,\langle \mathbf{w},\mathbf{e}_{i} \rangle=0$
$\langle \mathbf{w},\mathbf{e}_{i} \rangle=\langle \mathbf{v}-\mathbf{u},\mathbf{e}_{i} \rangle=\langle \mathbf{v},\mathbf{e}_{i} \rangle-\langle \sum_{j=1}^m \langle \mathbf{v},\mathbf{e}_{j} \rangle,\mathbf{e}_{j},\mathbf{e}_{i} \rangle$
