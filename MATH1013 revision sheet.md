LA:
$A\vec{x}=\vec{b}$
$x \in \mathbb{R}^n$
$b \in \mathbb{R}^m$

A transformation is injective  
$\iff A\vec{0}=\vec{0}$
$\iff$ there exists free variables
$\iff$ there is at least 1 column without a pivot 


A transformation is surjective IFF: every vector $\in \mathbb{R}^m$ can be written in terms of A 
$\iff$ REF(A) has a pivot in every row 
$\iff$ Col(A) $= \mathbb{R}^m$


if n = m, one to one implies onto and vice versa, which builds  the invertible matrix theorem 

invertible matrix theorem: $A_{m\times n}$ is invertible if there exists $B,C$ s.t $BA=I_{n}$ $\land AC=I_{m}$
$m=n\implies B=C=A^{-1}$
Note that this is not IFF, as $BA=I_{n}$ sometimes happens for $b$ = mxn and A = nxm


Dimension of null(A) = no of free variable 
Dim of col(A) = no of pivot columns 
Rank nullity theorem: dim of null space + dim col(A) = dim of the domain $\mathbb{R}^n$
Note that they are not subspaces related directly, as col $\in \mathbb{R}^m$and null $\subset \mathbb{R}^N$, but t