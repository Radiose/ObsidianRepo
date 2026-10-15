Recall that if $V$ is [[finite dimensional]], it has an [[orthonormal vectors|orthonormal basis]].

# Definition 
If $U$ is a [[vector subspace|subspace]], its orthogonal complement is denoted by $U^\perp$, and is a [[vector subspace|subspace]] such that $$U^\perp:=\{ \mathbf{v}\in V | \forall \mathbf{u} \in U \quad \langle \mathbf{u},\mathbf{v} \rangle=0 \}$$Exercise: show that $U^\perp$ is a subspace 

# Theorem 
if $U$ is [[finite dimensional]], then $V=U \oplus U^\perp$

### Proof 
$(1)$ $U + U^\perp=V$

let $\mathbf{v}\in V$, and $\{ \mathbf{e}_{1},\dots,\mathbf{e}_{n} \}$ be an [[orthonormal vectors|orthonormal basis]] of $V$
Define $\mathbf{u}=\langle \mathbf{v},\mathbf{e}_{1} \rangle\mathbf{e}_{1}+\dots+\langle \mathbf{v},\mathbf{e}_{m} \rangle\mathbf{e}_{m} \in U$
Define $\mathbf{w}:=\mathbf{v}-\mathbf{u}$ $\implies$$\mathbf{v}=\mathbf{u}+\mathbf{w}$

We can check that $\forall i \in \{ 1,\dots,m \} ,\langle \mathbf{w},\mathbf{e}_{i} \rangle=0$
$\langle \mathbf{w},\mathbf{e}_{i} \rangle=\langle \mathbf{v}-\mathbf{u},\mathbf{e}_{i} \rangle=\langle \mathbf{v},\mathbf{e}_{i} \rangle-\langle \sum_{j=1}^m \langle \mathbf{v},\mathbf{e}_{j} \rangle\mathbf{e}_{j},\mathbf{e}_{i} \rangle$
$= \langle \mathbf{v},\mathbf{e}_{i} \rangle-\sum_{j=1}^m \langle \mathbf{v},\mathbf{e}_{j} \rangle\langle \mathbf{e}_{j},\mathbf{e}_{i} \rangle$
$=\langle \mathbf{v},\mathbf{e}_{i} \rangle-\langle \mathbf{v},\mathbf{e}_{i} \rangle{1}=0$

$(2)$ $U\cap U^\perp=\{ \mathbf{0} \}$
Assume that $\mathbf{v}\in U \cap U^\perp$
Then $\langle \mathbf{v},\mathbf{v} \rangle=0$ (via orthogonality from def of $U^\perp$) 
$\iff \mathbf{v}=\mathbf{0}$
$\blacksquare$

# Corollary 
If $V$ is finite dimensional, then $\dim(V)=\dim(U)+\dim(U^\perp)$
Exercise: if $U$ is a subspace of $W$, and $W$ is a subspace of $V$, then $W^\perp \subset U^\perp$ 

# Theorem 2
$U=(U^\perp)^\perp$


### Proof 
let $\mathbf{u}\in U$, then $\langle \mathbf{u},\mathbf{v} \rangle=0\quad\forall \mathbf{v}\in U^\perp$
$\implies \mathbf{u}$ is orthogonal to all $\mathbf{v}\in U^\perp$
$\implies \mathbf{u} \in (U^\perp)^\perp$ 
Other dir:
Let $\mathbf{v}\in (U^\perp)^\perp$
We know that $V=U \oplus U^\perp$
$\implies \mathbf{v}=\mathbf{w}+\mathbf{u}$ for $\mathbf{w}\in U^\perp,\mathbf{u}\in U$
$\implies 0=\langle \mathbf{v},\mathbf{w} \rangle$ (by definition of orthogonality)
$\implies 0=\langle \mathbf{u}+\mathbf{w},\mathbf{w} \rangle=\langle \mathbf{u},\mathbf{w} \rangle+\langle \mathbf{w},\mathbf{w} \rangle=0+\langle \mathbf{w},\mathbf{w} \rangle$
$\implies \mathbf{w}=0$ by non degeneracy of [[inner product]]s
$\implies \mathbf{v}=\mathbf{u}\in U$

# Corollary 
$U \subset W \iff W^\perp \subset U^\perp$
$\implies$ (exercise)
$\impliedby$
$W^\perp \subset U^\perp \implies (U^\perp)^\perp \subset (W^\perp)^\perp$ (by exercise)
$\implies U \subset W$ by [[orthogonal complement#Theorem 2|the theorem above]]



# Theorem 3
if $V$ is finite dimensional, then $\phi:V\to V^V$ is an [[isomorphism]]. (where $\phi$ is the one in the [[conjugate linear involution]] note)

Under this [[isomorphism]], $\phi(U^\perp)$ is identified with $Ann(U)$ (the [[annihilator]])
IE, $\phi (U^\perp)=Ann(U)$

# Proof 
We aim to show that $\phi$ is injective. 
Assume that $v \in V$ is in $\ker(\phi)$
$\forall \mathbf{w}\in V,\phi(\mathbf{v})(\mathbf{w})=0$
In particular, for $\mathbf{w}=\iota(\mathbf{v}),0=\iota(\mathbf{v})(\iota(\mathbf{v}))=\langle \iota (\mathbf{v}),\iota(\mathbf{v}) \rangle\implies \iota(\mathbf{v})=0$
Note, $\iota(\mathbf{0})=0$, and $\iota$ is bijective so therefore $\mathbf{v}=0$. $\iota$ is bijective because $\iota^2=id_{v}$, implying that it has an inverse(itself) and via [[Invertible matrix theorem]], it must be bijective. 

Now, $\dim(V^V)=\dim(V)$, $\phi$ being injective implies $\phi$ is an [[isomorphism]].  

This concept can be also thought of by the theorem above. 
