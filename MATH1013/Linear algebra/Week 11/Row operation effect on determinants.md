Row operation effect on [[The determinant|determinant]]s

All of the following properties are defined by the corresponding [[elementary Matrix]] to each row operation.

Recall that there are 3 row operations, 

1: Addition of row to another row  - [[The determinant]] doesnt change 
2: Swapping of rows - changes the sign 
3: Scaling of the rows - scaled [[The determinant]] accordingly 


## Proofs 
The [[elementary Matrix]] for addition of one row to another is always either upper or lower triangular with 1s on the diagonal. Because its upper/lower triangular, it will always be the product of the 1s on the diagonal, and thus will always be equal to one. 
$$
\textbf{Proof 1: elementary matrices} \begin{aligned} A &\;\longmapsto\; \begin{bmatrix} 1 & & & & \\ & \ddots & & c & \\ & & 1 & & \\ & & & \ddots & \\ 0 & & & & 1 \end{bmatrix} A \\[10pt] \det \begin{bmatrix} 1 & & & c \\ & \ddots & & \\ & & \ddots & \\ 0 & & & 1 \end{bmatrix} &= 1 \cdot 1 \cdot 1 \cdots 1 = 1 \\[10pt] \det\!\left( \begin{bmatrix} 1 & & & c \\ & \ddots & & \\ & & \ddots & \\ 0 & & & 1 \end{bmatrix} A \right) &= \det \begin{bmatrix} 1 & & & c \\ & \ddots & & \\ & & \ddots & \\ 0 & & & 1 \end{bmatrix} \det A = \det A \end{aligned}$$





proof 2, based off the [[Axiomatic definition of the determinant]] on the [[linearity]] of addition 



$$ \begin{aligned} &\begin{bmatrix} a_{11} & \cdots & a_{1n} \\ \vdots & & \vdots \\ a_{i1} & \cdots & a_{in} \\ \vdots & & \vdots \\ a_{j1} & \cdots & a_{jn} \\ \vdots & & \vdots \\ a_{n1} & \cdots & a_{nn} \end{bmatrix} \xrightarrow{R_i + cR_j} \begin{bmatrix} a_{11} & \cdots & a_{1n} \\ \vdots & & \vdots \\ a_{i1}+ca_{j1} & \cdots & a_{in}+ca_{jn} \\ \vdots & & \vdots \\ a_{j1} & \cdots & a_{jn} \\ \vdots & & \vdots \\ a_{n1} & \cdots & a_{nn} \end{bmatrix} \\[15pt] &\det \begin{bmatrix} a_{11} & \cdots & a_{1n} \\ \vdots & & \vdots \\ a_{i1}+ca_{j1} & \cdots & a_{in}+ca_{jn} \\ \vdots & & \vdots \\ a_{j1} & \cdots & a_{jn} \\ \vdots & & \vdots \\ a_{n1} & \cdots & a_{nn} \end{bmatrix} \\[10pt] &= \det \begin{bmatrix} a_{11} & \cdots & a_{1n} \\ \vdots & & \vdots \\ a_{i1} & \cdots & a_{in} \\ \vdots & & \vdots \\ a_{j1} & \cdots & a_{jn} \\ \vdots & & \vdots \\ a_{n1} & \cdots & a_{nn} \end{bmatrix} + \det \underbrace{\begin{bmatrix} a_{11} & \cdots & a_{1n} \\ \vdots & & \vdots \\ ca_{j1} & \cdots & ca_{jn} \\ \vdots & & \vdots \\ a_{j1} & \cdots & a_{jn} \\ \vdots & & \vdots \\ a_{n1} & \cdots & a_{nn} \end{bmatrix}}_{=\, 0} \end{aligned}$$

Note that for the second determinant on the bottom, rows i and j are the same (scalar multiples), thus the determinant is 0.


## Scalar multiples 
One thing we should note is that $\det(cA) \not= c\det A$
![[Pasted image 20260525171027.png]]

The image above helps to show this. A singular row scale being taken out will scale it once. Every row being scaled will scale the determinant by $c^n$
