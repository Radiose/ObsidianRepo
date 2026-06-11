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

Calculus:

Recall that you fix a codomain to make a function surjective. 
Sometimes you also have to fix the domain. 
EG $\sqrt{ 2x+1 }$
We fix domain to be all number ST 2x+1 is greater than or equal to zero 
remember that $(\sqrt{ x })^2=x$, and $\sqrt{ x^2 }= |x|$
Always verify that 


Critical points: A point c in the domain of f such that f'(c) = 0 OR f'(c) DNE. 


![[Pasted image 20260606141431.png]]
One and two are circles with the equaion 

Note that limits are in terms of one variable. lim h-> 0 f(x) when you use lhopitals rule will have f(x) = 0

For IBP: Often, with e^X. the integrand is repeated, which allows you to fully solve. 

Can prove injectivity with always increasing derivatives. means function is strictly increasing, and thus injective 

arcsin always takes off right side of unit circle 

Revisit the lontief model 


$\ln(f(x))=\frac{f'(x)}{f(x)}$

Remember to use implicit differentiation in logarithmic differentiation 
Remember to resub y = initial equaiton when done.

sub dx early in trig sub 



A quadrilateral is a parallelogram IFF it has two parallel sides that are congruent -find vectors between them 


Determinant story: 
We first talked about finding the area of a parallelogram in $\mathbb{R}^2$
We did this through demonstrating proofs that the vectors are both linear 
Then showed scalars are linear 


Remember that to get argument of complex number, arctan has a restricted domain from -pi/2 to pi/2. 
arcsin : -1 1 -> \[-pi/2 pi/2]
	arccos: -1 1 -> \[0, pi] 
	arctan: R -> (-pi/2 pi/2)




Subspace and solution set 
If a solution set of a system Ax = b is a plane, then if we treat it as a linear subspace, then Ax = 0 is a solution and thus the solution set is identical to the null space. 


If a matrix is not injective, then there are infinitely many solutions for any b 
If a matrix is not surjective, then some bs are not present. 

