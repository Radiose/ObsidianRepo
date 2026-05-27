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
Note that they are not subspaces related directly, as col $\in \mathbb{R}^m$and null $\subset \mathbb{R}^N$, but the dimensions are through rank nullity


Notes of fundamental theorem of algebra:
If all coefficients of the polynomial are real, then all complex numbers must come in complex conjugate pairs. If some coefficients are complex, then its not guaranteed 

Lontief econ mod:
if the model has entries such that the entries sum up to be strictly less than 1, the matrix  I_n-C is invertible. Because of this, we can solve based on the demand.
"In the exam, you're going to be given a very concrete matrix C. You set up the equation and you have to solve that equation to make sure its invertible and you have to solve for the equation to find the total production satisfying a certain demand."

You have to solve some equation like $I-C\times \vec{y}=\vec{d}$

We never required I-C to be strictly invertible for any specific problem, you have to analyse whether it is invertible in general 

