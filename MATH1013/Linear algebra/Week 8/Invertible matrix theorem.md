Proving an [[Inverse matrix]]
Every [[Statement]] regarding the invertibility of a [[matrix]] can be thought of as a definition, with the others being regarded as [[theorem]]s. 

Some definitions:
A (square) [[matrix]] is invertible if there is a matrix B, such that AB = BA = $I_{n}$
Definitions of [[Inverse matrix]]:
0: A is invertible ($\exists B \ \ AB = BA=I_{n}$)
1: $A \vec{x} = 0$ has only the trivial solution (A is [[linearly independent]])
2: A is row equivalent to $I_{n}$
We can prove these definitions via showing $0 \iff 1 \iff 2$

# Demonstrating $0 \implies 1$
The idea: Suppose A is invertible, show that $A \vec{x} = 0$ has only the trivial solution. 

A is invertible, thus there exists a matrix B such that BA = $I_{n}$ =AB 
B is also $n \times n$ dimensions (Same as A)

$A \vec{x}=0$
$\iff BA \vec{x} = B0$
$I_{n} \vec{x} = 0$
thus $\vec{x} = 0$

Thus, we have proven that $0 \implies 1$
# Demonstrating $1 \iff 2$

The idea: suppose a $n\times n$ matrix exists and $A \vec{x} = 0$ only has the trivial solution. We want to prove that RREF(A) = $I_{n}$

Using logical deduction:

Suppose that $A \vec{x}=0$ has only the trivial solution 
$\iff$ $RREF(A)$ has a pivot in each column(definition of [[linearly independent]])
$\iff RREF(A)$ has a pivot in each row (A is an $n \times n$ matrix)
$\iff RREF(A) = I_{n}$

# Demonstrating $1 \implies 0$
The idea: suppose $A \vec{x}=0$ has only the trivial solution and A is an $n \times n$ matrix. Show that A is invertible ($\exists B\ \ AB = BA = I_{n}$).

$AB = I_{n} \iff$ solve $A[\vec{b_{1}}\vec{b}_{2}\dots \vec{b_{n}}]=[\vec{e_{1}}\vec{e_{2}}\dots \vec{e_{n}}]$
## show $A \vec{b} = \vec{e}$ is consistent 
Given the fact that $A \vec{x} = 0$ has only the 0 solution, we aim to show that $A \vec{b}=\vec{e}$ is [[Consistent linear system]].

REF(A) has a pivot in each column and each row. (definition of [[linearly independent]] and A is square matrix)  
$\iff A \vec{b} =\vec{e_{1}}$ is always consistent for any $\vec{e} \in \mathbb{R}^n$
$\iff \exists$ an $n \times n$ matrix $B$ such that $AB = I_{n}$
## Show $AB = I_{n} \implies BA = I_{n}$
$AB = I_{n}$
$\iff  BAB = BI_{n}$
$\iff BAB = B$
$\iff BA = I_{n}$


## Show $XB = B \implies X = I_{n}$

Now we show that $BA = I_{n}$ (if $AB = I_{n}$), then $BAB = BI_{n}$

We try to show that $XB =B \implies X = I_{n}$
If $XB = B \implies XB \vec{x} = \vec{x}$ for any $\vec{x} \in \mathbb{R}^n$
If all $\vec{x} \in \mathbb{R}^n$ can be written as $B \vec{x}$, then $X \vec{y} =\vec{y}$ for any $\vec{y} \in \mathbb{R}^n$
$\implies X = I_{n}$




## Show $\forall \vec{b}\in \mathbb{R}^n \ \ \vec{B}x=\vec{b}$
Now, we have to show that all $\vec{x}\in \mathbb{R}^n$ can be written as $B \vec{x}$. We show that the [[Transformation]] defined B is a [[Surjective transformation]].

If $AB = I_{n}$, show that $col(B)=\mathbb{R}^n$


$AB = I_{n} \implies RREF(A) = I_{n} \implies RREF(A)$ has a pivot in every column and row.
$\iff$ the [[Transformation]] defined by A is an [[Injective transformation]]. $\iff$ A is [[Surjective transformation]] $\iff$ A is a [[Bijective Transformation]].

Any $\vec{b} \in \mathbb{R}^n$ can be uniquely written as $\vec{b} = A \vec{x}$.

$AB = I_{n}$ is a bijection, as the identity transformation must be bijective, as it sends every vector to itself. 


## Putting it all together

If $AB = I_{n}$,  A is a bijection, and AB is a bijection, thus B is also a [[Bijective Transformation]].  Thus, we have shown that  $\forall \vec{y} \in\mathbb{R}^n$ can be written as $B \vec{x}=\vec{y}$.
