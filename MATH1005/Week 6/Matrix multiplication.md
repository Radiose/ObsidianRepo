---
{}
---
Matrix multiplication 
### MATH1005:
We design [[Matrix]] multiplication so that it corresponds with the [[composition of Functions|composition]] of [[Linear functions]]

You must have the same number of columns in the first matrix as rows in the second to be able to multiply matrixes

Matrix A x [[Matrix]] B is not the same as matrix B times matrix A.


The basics of matrix multiplication are as follows:
$\begin{matrix} [1, 2]   \\  [3,4]\end{matrix} \times \begin{matrix} [a,b]  \\ [c ,d]\end{matrix} = \begin{pmatrix}a+2c \ \ \ b+2d \\ 3a +4c\ \ \ 3b+4d\end{pmatrix}$


Remember:
Matrix multiplication is not commutative, but associative 
So *MN $\not=$ NM*
BUT 
$M(NP) = (MN)P$
This is a direct consequence of the correspondence to linear function composition. F $\circ$ (G $\circ H$) = (F $\circ$ G) $\circ$ H.
You can move the brackets around, but the *order* of matrices must be the same. 

### MATH1013
The standard matrix of composed [[Linear transformation]]s 

thus the [[composition of Functions|composition]] of two linear transformations = $(BA)\vec{x}$ = $B(A\vec{x})$ via associativity laws.
$B(A \vec{x}) = B(x_{1}v_{1}+x_{2}v_{2}\dots x_{n}v_{n})$
$(BA)\vec{x}= x_{1}Bv_{1}+x_{2}Bv_{2}\dots x_{nBv_{n}}$
So, $BA$ = $[B \vec{v}_{1}B \vec{v}_{2}\dots B\vec{v}_{n}]$
Thus, by multiplying two matrices, you will multiply every row of a [[Matrix]] by another. 

So, [[Matrix multiplication]] is essentially just related to composition of [[Linear transformation]]s.

Thus, you can only multiply matrices together, if you can compose the matrices together as [[Linear transformation]]s.

For this reason, a 3x2 and a 3x2 [[Matrix]] cannot be multiplied together, as the dimensions dont obey the laws of [[composition of Functions|composition]] of [[Linear transformation]].

If $A = 3 \times 2$ and $B = 2 \times 3$
$AB = 3 \times 3$
$BA = 2 \times 2$


Square matrices as a result, are the only matrix that can be multiplied by itself. 