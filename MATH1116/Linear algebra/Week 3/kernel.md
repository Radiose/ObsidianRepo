---
aliases:
  - null space
---
Null space is **the set of all solutions to the homogeneous equation Ax = 0**, or geometrically, the linear subspace. You can obtain a null space via obtaining a [[parametric vector form]] of the solution for Ax = 0. 

# Definition 

The kernel of a [[linear map]] $T:V \to W$ is denoted by $ker(T):= \{ \mathbf{u} \in V: T(\mathbf{u})=\mathbf{0}\}$

# Remarks
The kernel of $T$ is a [[vector subspace|subspace]] of $V$


# Theorem 
A [[function|map]] $T: V\to W$ is [[Injective transformation]] $\iff \ ker(T)={\{ \mathbf{0} \}}$

Proof: $\implies$ 
If $\mathbf{u} \in$ $ker(T)$, 

$T(\mathbf{u})=\mathbf{0}=T(\mathbf{0})\implies\mathbf{u}=\mathbf{0}$ definition of injectivity

$\impliedby$
Assume $T(\mathbf{u})=T(\mathbf{v})$
$\mathbf{0}=T(\mathbf{u})-T(\mathbf{v})=T(\mathbf{u}-\mathbf{v})$ If $\mathbf{0}=T(\mathbf{u}-\mathbf{v})$, then they must be in the kernel. 
$\mathbf{u}-\mathbf{v}\in ker(T)$
But $ker(T)=\{ \mathbf{0} \}$, so $u=v$, and thus $T$ is injective. 
