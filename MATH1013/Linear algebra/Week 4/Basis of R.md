$e_{1}e_{2}e_{3}\dots$ is a basis of $\mathbb{R}^n$
Can be expressed - can be uniquely expressed. Is an [[Injective Function|injective]] correspondence.


Theorem of basis 

if $\{ v_{1}\dots v_{m} \}$  is a bases of $\mathbb{R}^n$, then there must be exactly n bases in the collection.

Intuitively, this can be demonstrated through the following 
$m<n \iff span\{ v_{1} v_{2}\dots v_{m}\} \not= \mathbb{R}^n$ - every vector in R has to expressed 
when m > n, $\{ v_{1},v_{2}\dots v_{m} \}$ is [[Linearly dependent]].  - has to be unique. The map is not [[Injective Function|injective]].


## Expressing a vector with respect to a basis 

If you think about matrices as systems of linear equations, and a basis as a possible way to represent a space, then you can use a basis to represent a vector. If a basis is $\mathcal{B}$, then finding the weights to represent in terms of $\mathcal{B}$ is simply a method of solving $\mathcal{B}\vec{c}=\vec{v}$.



Consequences of basis:

A basis B of H must satisfy:
So, the span$\{ v_{1},v_{2}\dots v_{k} \}$ = H
For every $\vec{v}\in H$ it can uniquely written as $\vec{v}=x_{1}v_{1}+x_{2}v_{2}\dots x_{k}v_{k}$
$\vec{0}\in H$ can be uniquely written as a [[Linear combination of vectors]] $\{ v_{1} \dots v_{k \}}$
Therefore, $\vec{0}=x_{1}v_{1}\dots+x_{k}v_{k}$ has a unique solution. $\implies$ $v_{1}v_{2}v_{k}$ are [[linearly independent]]


Additionally
$B = \{ v_{1},v_{2}\dots v_{k} \}$ is a basis $\iff$ span$\{ v_{1},v_{2}\dots v_{k} \}$= H $\land$ $v_{1}\dots v_{k}$ are [[linearly independent]]

Definition if $B = \{ v_{1},v_{2}\dots v_{k} \} \subset H$ is a basis of the [[Linear subspace]] $H \in \mathbb{R}^n$,t hen for any $\vec{v}\in H$ can be expressed as 

Two dimensional expression of a basis 

all basis of $\mathbb{R}^2$ are in the format $B=V_{1}V_{2}$ where both are non zero, and point in different directions 

![[Basis of a nullspace]]

![[Basis of a column space]]

![[Rank nullity theorem]]