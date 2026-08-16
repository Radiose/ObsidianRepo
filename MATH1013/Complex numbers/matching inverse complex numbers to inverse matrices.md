recall that a $2\times 2$ [[matrix]] can be converted to an [[Inverse matrix]] iff its columns are [[linearly independent]], also iff its [[The determinant|determinant]] is non zero. 

If [[The determinant]] is non zero, then $\begin{bmatrix}ab \\ cd\end{bmatrix}$ is invertible and its inverse is the following $\frac{1}{ad-bc}\begin{bmatrix}d \ -b \\ -c \ a\end{bmatrix}$
This can be proven by $A \cdot A^{-1}=I_{n}$
We check that $x+yi$ is invertible iff det($\begin{bmatrix}x \ -y \\ y\ \ \ \ x\end{bmatrix}$ )$\not=0$
$(x \cdot x) -(-y \cdot y) \not=0$
$\implies x^2+y^2 \not=0$
note that this is (almost) the modulus of Z as defined through the [[Geometric interpretation of complex numbers]].

The inverse of the [[Standard Matrix]] of complex numbers should also be identical to the [[Standard Matrix]] of [[Inverse complex numbers]]
inverse of z = $\frac{x}{x^2+y^2}-i \frac{y}{x^2+y^2}$
inverse of standard matrix: $\frac{1}{x^2+y^2}$$\begin{bmatrix}x \ \ -y  \\ y\ \ \ \ x\end{bmatrix}$
$= \begin{bmatrix} \frac{x}{x^2+y^2}\ \ \frac{y}{x^2+y^2}  \\ -\frac{y}{x^2+y^2}\ \ \frac{x}{x^2+y^2}\end{bmatrix}$
We can see that we have the real components on the diagonal, and the imaginary on the inverse diagonal 
