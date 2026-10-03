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
$\langle \mathbf{u},\mathbf{v} \rangle=\overline{\langle \mathbf{v},\mathbf{u} \rangle}\quad \forall \mathbf{u,v}\in V$ , where the RHS is the [[complex conjugate]] (conjugate symmetry)

#### Consequences:
Additivity and homogeneity imply that a fixed $\langle \_,\mathbf{v} \rangle$ is a [[linear map]]
Additionally, it allows for [[orthogonal vectors|orthogonal]] projection which leads to things like [[Gauss least squares]]


### Examples 
**Ex. 1)** $V = \mathbb{F}^n$; pick some $c_1, \dots, c_n \in \mathbb{R}_{>0}$. Then

$$
\left\langle
\begin{bmatrix} u_1 \\ \vdots \\ u_n \end{bmatrix},
\begin{bmatrix} v_1 \\ \vdots \\ v_n \end{bmatrix}
\right\rangle
:= c_1 u_1 \overline{v_1} + \cdots + c_n u_n \overline{v_n}
$$

defines an inner product.

**1')** If some $c_i < 0$, then 1 is not an inner product.

2: $V=P(\mathbb{F}),$ then $\langle p,q \rangle=\int_{0}^\infty p(x)\overline{{q}(x)}\ e^{-x}dx$ is an inner product 

3: $V = C([a,b],\mathbb{F}):=\{ f:[a,b] \to \mathbb{C} | f\text{ is continuous}\}$
	Then, $\int _{a}^b f(x) \overline{g(x)}:=\langle f,g \rangle$ defines an inner product 


![[inner product space]]