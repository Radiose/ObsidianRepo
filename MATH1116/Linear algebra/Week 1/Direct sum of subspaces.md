---
aliases:
  - direct sum
  - internal sum
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
We want to show $\mathbf{u}-\mathbf{v_{1}}=0$ and $\mathbf{w}-\mathbf{v_{2}}=0$
Suppose $0=\mathbf{u}+\mathbf{w}$

KEY MOVE:
This implies that $\mathbf{u} \in U=\mathbf{-w}\in W$, thus $\mathbf{u}\in U\cap W$. Recalling $U \cap W = \{0  \}$ $\mathbf{u}-\mathbf{w}=0$ (which can be generalised to the vectors created through subtraction). Hence, $\mathbf{u}=\mathbf{w}$.


$\impliedby$
Suppose that $U+W$ is a direct sum. 
If $\mathbf{v}\in U \cap W$, then $$\mathbf{0}=\mathbf{v}+(-\mathbf{v})$$
here $\mathbf{v}\in U$ and $-\mathbf{v}\in W$. Since the representation of $\mathbf{0}$ as an element in $U \oplus W$ is unique, and $\mathbf{0}=\mathbf{0}+\mathbf{0}$ is an obvious representation, then $\mathbf{v}=\mathbf{-v}=\mathbf{0}$. Thus, $U \cap W=\{ \mathbf{0} \} \blacksquare$

The point with this direction of the proof is that $\mathbf{0}$ can only be represented one way via the direct sum property, thus $\mathbf{v}$ must equal $\mathbf{0}$


IMPORTANT:
The following is equivalent. The direct sum of vector spaces, as well as the internal direct sum of subspaces are identical, where we denote a subspace as $U'_{i}:=\{ (\mathbf{0},\dots u_{1},\dots,\mathbf{0}) \} \subset U_{1}\oplus U_{2}\oplus\dots \oplus U_{n}$


![[Direct sum of vector spaces]]