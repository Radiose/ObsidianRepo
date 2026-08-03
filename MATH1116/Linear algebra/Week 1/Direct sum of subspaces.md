---
aliases:
  - direct sum
---
Suppose $U_{1},\dots,U_{m}$ are [[vector subspace|subspace]]s of $V$. The sum $U_{1}+\dots+U_{m}$ is called the (internal) direct sum if each element of $U_{1}+\dots+{U_{m}}$ can be written in only one way as a sum $\mathbf{u_{1}}+\dots+\mathbf{u_{m}}$
If $U_{1}+\dots+{U_{m}}$ is a direct sum, then we write $U_{1} \oplus\dots \oplus U_{m}$ with the $\oplus$ notation indicating this is a direct sum.

# Theorem 1
Suppose $U$ and $W$ are subspaces of $V$. Then, $U +W$ is a direct sum if and only if $U \cap W=\{ 0 \}$
proof:
$\implies$
Suppose $U \cap W=\{ 0 \}$.
we write
$\mathbf{v}=\mathbf{u}+\mathbf{w}$ for some $\mathbf{u}\in U,\mathbf{v}\in V$
We show that this representation is unique, suppose that we also have 
$\mathbf{v}=\mathbf{v_{1}}+\mathbf{v_{2}}$
Subtracting these 
$\mathbf{0}=(\mathbf{u}-\mathbf{v_{1}})+(\mathbf{w}-\mathbf{v_{2}})$
