# SERIES CONVERGENCE THEOREMS 
1: $x_{j}\xrightarrow[j \to \infty]{}0$
2: $\lim_{ j \to \infty } \frac{x_{j}}{y_{j}}=\ell$, $\sum x_{j}$ converges $\iff \sum y_{j}$ converges. 
3: Let $(x_j)_{j\in\mathbb{N}}, (y_j)_{j\in\mathbb{N}} \in \mathbb{R}^{\mathbb{N}}$ be such that $0 \leq x_j \leq y_j, \forall j \in \mathbb{N}$.
Then $\sum_{j=0}^{\infty} y_j$ converges implies $\sum_{j=0}^{\infty} x_j$ converges.

TESTS:
INTEGRAL 
RATIO - things with factorials, etc 


NEGATIVE TERMS: 
Abs convergence $\implies$ convergence, but not conversely 

summation by parts theorem 
1: a_n approaches infty 



SUMMATION BY PARTS 


# Geometric series 
$\sum x^n$ converges $\iff x<1$
$\sum$


# LA 
A subset of a vector space is a vector subspace(subspace) if it is a vector space with respect to the same operations as V 

A subset is a vector subspace iff:
	i) $\mathbf{0}\in U$
	ii) $\mathbf{u,w} \in U \implies \mathbf{u}+\mathbf{w}\in U$
	iii) $\lambda \in F$, $\mathbf{u}\in U \implies \lambda \mathbf{u} \in U$

Sum of subsets:

Let $U_{1},\dots,U_{m} \subset V$ (just subsets) and **nonempty**,
their sum is defined as $\{ \mathbf{u_{1}}+\dots+\mathbf{u}_{m}|\mathbf{u_{1}}\in U_{1},\dots, \mathbf{u}_{m}\in U_{m}\}$
In other words, the sum is the set of all possible sums of elements of $U_{1},\dots,U_{m}$


Internal direct sum 
Suppose $U_{1},\dots,U_{m}$ are [[vector subspace|subspace]]s of $V$.
The sum $U_{1}+\dots+U_{m}$ is called the (internal) direct sum if each element of $U_{1}+\dots+{U_{m}}$ can be written in only one way as a sum $\mathbf{u_{1}}+\dots+\mathbf{u_{m}}$
If $U_{1}+\dots+{U_{m}}$ is a direct sum, then we write $U_{1} \oplus\dots \oplus U_{m}$ with the $\oplus$ notation indicating this is a direct sum.




External direct sum 

Suppose $U_{1},\dots,U_{m}$ are [[vector space]]s. We define their direct sum $U_{1}\oplus\dots \oplus U_{m}$ as the set of **tuples** $(\mathbf{u}_{1},\dots,\mathbf{u_{m}})$ with $\mathbf{u_{i}}\in U_{i}$. We endow this set with the element wise operations of addition and scalar multiplication. 
$(\mathbf{u}_{1},\dots,\mathbf{u_{m}})+(\mathbf{v}_{1},\dots,\mathbf{v_{m}}):=(\mathbf{u}_{1}+\mathbf{u_{m}},\dots,\mathbf{u_{m}+\mathbf{v_{m}}})$
$\lambda \cdot(\mathbf{u}_{1},\dots,\mathbf{u_{m}}):=(\lambda \mathbf{u_{1}},\dots,\lambda \mathbf{u}_{m})$




Linear combination 

Span 

Finite dimensional 

Linear independence 
c1v1 + ... + cn vn = 0 iff c = 0


Basis 
Linearly independent, spanning set 


Dimension 
Dimension of an internal direct sum: dim(u + w) = dim(u) + dim(w)
Dimension of a non direct sum of subspace u+ w = dim(u)+dim(w)-dim(unw)