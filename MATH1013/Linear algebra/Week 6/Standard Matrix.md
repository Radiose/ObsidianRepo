---
{}
---
Standard [[Matrix]]
For a [[Linear transformation of R n]] T, we can get the standard matrix of T from $A = [t(\vec{e}_{1})\dots t(\vec{e}_{n})]$, where e are columns in the [[basis of R]]. 

Theorem: 
T(x) = A$\vec{x}$
if T is a [[Linear transformation of R n]]

Applying [[linearity]]:
$T(\vec{x})= A \vec{x}$
$\iff$
T($\begin{pmatrix}x_{1}  \\  x_{2}  \\  \dots  \\  x_{m}\end{pmatrix}$)=$T(x_{1}e_{1}+x_{2}e_{2}\dots x_{n}\vec{e}_{n})$= $xT(\vec{e_{1}})+\dots x_{n}T(\vec{e_{n}}) = A \vec{x}=T(\vec{x})$




This is easy to do using the standard [[basis of R]] of the [[Transformation]] 

So if someone gives the [[Transformation]]s domain and codomain, you can find the [[Standard Matrix]] using the standard basis. 


## Steps to finding a [[Standard Matrix]]
Given some examples of the [[Linear transformation of R n]], we relate each standard [[basis of R]] [[vector]] to the vectors (find some combination of vectors that gives $e_n$). We take the scalar multipliers, and then apply them to the vectors that are the products. Then, we sum them together. 