---
aliases:
  - dot product
cssclasses:
---
# Analysis simplification
## Definition 
The inner product of two [[vector]]s $(x_{1},\dots.,x_{n})$ and $(y_{1},\dots,y_{n})$ is denoted 
$$\langle (x_{1},\dots,x_{n}),(y_{1},\dots,y_{n}) \rangle:=\sum_{j=1}^n x_{j}y_{j}$$



# Linear algebra definition 
The inner product is the vector definition of multiplication. 
Suppose $V$ is a [[vector space]] over $\mathbb{F}$. An inner product on $V$ is a [[function]] $V \times V \to \mathbb{F}$ that takes each ordered pair $\mathbf{(u,v)}$ of elements of $V$ to a scalar $\langle \mathbf{u}, \mathbf{v} \rangle\in \mathbb{F}$ and has the following properties:
$\langle \mathbf{v,v} \rangle\geq {0}$ (positiveness)
$\langle \mathbf{v,v} \rangle=0 \iff \mathbf{v}=\mathbf{0}$ (definiteness)
$\langle\mathbf{u+v,w}  \rangle=\langle \mathbf{u} ,\mathbf{w}\rangle+\langle \mathbf{v} ,\mathbf{w}\rangle$ (additivity)
$\langle \lambda \mathbf{u},\mathbf{v} \rangle=\lambda \langle \mathbf{u},\mathbf{v} \rangle\forall \lambda \in \mathbb{F}$ and all $\mathbf{u},\mathbf{v}\in V$ (homogeneity)
$\langle \mathbf{u},\mathbf{v} \rangle=\overline{\langle \mathbf{v},\mathbf{u} \rangle}\quad \forall \mathbf{u,v}\in V$ (conjugate symmetry)


![[Inner product space]]