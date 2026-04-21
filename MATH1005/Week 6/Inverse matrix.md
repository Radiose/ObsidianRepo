Inverse matrix 
An inverse [[Matrix]] is a method to solve a system of linear equations 
This matrix $A^{-1}$ is an inverse of A in the following sense 
An inverse, if one exists, of a [[Matrix]] $A \in M_{n}(\mathbb{Q})$ is a matrix $A^{-1} \in M_{n}(\mathbb{Q})$ with the property that $A^{-1}A = AA^{-1}=I_{n}$, where *I* is the [[Identity matrix]]

Note, that if an $A^{-1}$ exists and Ax = b then 
x = lx = $(A^{-1}A)x=A^{-1}(Ax) = A^{-1}b$


#### Existence of an [[Inverse matrix]]

The nature of an inverse matrix (IE that $AA^{-1}=I_{n}$ and that $A^{-1}A = I_{n}$) ensure that only square [[Matrix|matrices]] have inverses. 

Not every square matrix has an inverse 
***A* has an inverse if and only if the [[Function]] $A \mapsto Ax$ is a [[Bijective Transformation]]**
This is why it must be a square matrix, as it all relates back to [[Null space]] and [[Column space]] of said [[Transformation]]. 


A matrix can have at most one inverse 

Computing the [[Inverse matrix]]
A matrix A = $\begin{pmatrix}a, b \\ c,d\end{pmatrix} \in M_{2}(\mathbb{Q})$ has an inverse IFF ad-bc $\not=0$ and in this case, 
$A^{-1} =\frac{1}{ad-bc}\begin{pmatrix}\ d,\ \ -b \\ -c,\ \ a\end{pmatrix}$

