---
aliases:
  - orthonormal
  - orthonormal basis
---
# Definition 
A set of vectors $\{ \mathbf{e_{1}},\dots,\mathbf{e}_{n} \}$ in $V$ are orthonormal if $\langle \mathbf{e}_{i},\mathbf{e}_{j} \rangle=\delta_{i,j}$


# Corollary
Recall the Pythagorean theorem ([[norm#Theorem (Pythagorean)|here]])
If $\{ \mathbf{e}_{1},\dots,\mathbf{e}_{n} \}$ is [[orthonormal vectors|orthonormal]], then $\lVert a_{1}\mathbf{e}_{1}+\dots+a_{n}\mathbf{e}_{n} \rVert= \lvert a_{1} \rvert^2+\dots+\lvert a_{n} \rvert^2$
You can think about this with the following slogan: In orthonormal coordinates, the norm $=$ [[Euclidian norm]].

### Proof 
$\lVert a_{1}\mathbf{e}_{1}+\dots+a_{n}\mathbf{e}_{n} \rVert^2=\langle  \sum a_{i}\mathbf{e}_{i},\sum a_{j}\mathbf{e}_{j}\rangle=\sum_{i,j} a_{i}\bar{a}_{j}\langle \mathbf{e}_{i},\mathbf{e}_{j} \rangle$
=$\sum_{i=j}a_{i}\bar{a}_{j}=\sum \lvert a_{i} \rvert^2$

# Corollary 
An [[orthonormal vectors|orthonormal]] set is [[linearly independent]]
### Proof
let $\{ \mathbf{e_{1}},\dots,\mathbf{e}_{n} \}$ be orthonormal 
Suppose $a_{1}\mathbf{e}_{1}+\dots+a_{n}\mathbf{e}_{n}=\mathbf{0}$
Then $0=\lVert \mathbf{0} \rVert^2 = \left\lVert  \sum a_{i}\mathbf{e}_{i}  \right\rVert^2=\sum \lvert a_{i} \rvert^2\implies a_{i}=0\forall i$ 


# Corollary 
If $\dim(V)=n$ and $\{\mathbf{e}_{1},\dots,\mathbf{e}_{n}  \}$ is [[linearly independent]], then $\{ \mathbf{e_{1}},\dots,\mathbf{e}_{n} \}$ is a [[basis]]
### Proof 
via [[the basis theorem]]


# Theorem 
If $\dim(V)=n<\infty$, then $V$ has an [[orthonormal vectors|orthonormal basis]]
### Proof 
This proof uses the Graham-Schmidt procedure. 

Suppose $V$ is [[finite dimensional]]. Choose some basis $\{ \mathbf{v}_{1},\dots,\mathbf{v}_{n} \}$ of $V$
Let $\mathbf{e}_{1}=\frac{\mathbf{v_{1}}}{\lVert \mathbf{v}_{1} \rVert}$. Note that $\lVert \mathbf{e}_{1} \rVert=\left\lVert  \frac{\mathbf{v}_{1}}{\lVert \mathbf{v}_{1} \rVert}  \right\rVert=\frac{1}{\lVert \mathbf{v}_{1} \rVert}\cdot \lVert \mathbf{v}_{1} \rVert=1$

For $j=2,..,m$, define $\mathbf{e}_{j}$ inductively by $$\mathbf{e}_{j}=\frac{\mathbf{v}_{j}-\langle \mathbf{v}_{j},\mathbf{e}_{1} \rangle\mathbf{e}_{1}-\dots-\langle \mathbf{v}_{j},\mathbf{e}_{j-1} \rangle\mathbf{e}_{j-1}  }{\lVert \mathbf{v}_{j}-\langle \mathbf{v}_{j},\mathbf{e}_{1} \rangle\mathbf{e}_{1}-\dots-\langle \mathbf{v}_{j},\mathbf{e}_{j-1} \rangle\mathbf{e}_{j-1} \rVert }$$
If we can show that $\{ \mathbf{e}_{1},\dots,\mathbf{e}_{m} \}$ is an orthonormal set of vectors in $V$ such that $span\{  \mathbf{v}_{1},\dots,\mathbf{v}_{j}\}=span \{ \mathbf{e}_{1},\dots,\mathbf{e}_{j} \}$ for $j=1,\dots,m$, then $\{ \mathbf{e}_{1},\dots,\mathbf{e}_{m} \}$ is a basis. 
