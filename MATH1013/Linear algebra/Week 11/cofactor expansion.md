
We aim to determine a formula for the determinant of the [[Matrix]] shown below
$\det \begin{bmatrix}a_{11} \ a_{12} \ a_{13}  \\ a_{21} \ a_{22} \ a_{23}  \\ a_{31} \ a_{32} \ a_{33}\end{bmatrix}$ = $a_{11}a_{22}a_{33}-a_{11}a_{23}a_{32}-a_{12}a_{21}a_{33}+a_{13}a_{21}a_{32}+a_{12}a_{23}a_{31}-a_{13}a_{22}a_{31}$


We group these together as such 
$$\begin{aligned}
&= a_{11}(a_{22}a_{33} - a_{23}a_{32}) \\
&\quad - a_{12}(a_{21}a_{33} - a_{23}a_{31}) \\
&\quad + a_{13}(a_{21}a_{32} - a_{22}a_{31}) \\
&= a_{11} \det \begin{bmatrix} a_{22} & a_{23} \\ a_{32} & a_{33} \end{bmatrix} - a_{12} \det \begin{bmatrix} a_{21} & a_{23} \\ a_{31} & a_{33} \end{bmatrix} + a_{13} \det \begin{bmatrix} a_{21} & a_{22} \\ a_{31} & a_{32} \end{bmatrix}
\end{aligned}
$$
(as determinant of 2x2 is defined as ad-bc)

What we aim to do is to generalise this.
## Cofactor expansion definition 

$\det \begin{bmatrix}a_{11}a_{21}\dots a_{n_{1}} \\  \\  \\  \\ a_{n_{1}}\ \ \dots a_{nn}\end{bmatrix}$
$A_{ij}$ is defined as the matrix obtained for A by deleting the $i$th row and the $j$th column 
We define $C_{ij} = (-1)^{i+j}\det A_{ij}$ 
$\det A = a_{11}C_{11}+a_{21}C_{21}\dots a_{n_{1}}C_{n_{1}}$
as cofactor expansion *with respect to the first column*

Cofactor expansion is a powerful tool for proofs, but not super useful for raw calculations.

[[theorem]]

Pick any col of A $\begin{bmatrix}a_{1i}  \\  a_{21}a. \\ . \\ . \\ . \\ a_{ni}\end{bmatrix}$
We have $\det A = a_{1i}C_{1i}+a_{2i}C_{2i}+\dots+a_{ni}C_{ni}$ 
and additionally, $\det A=a_{j{1}}C_{j 1} + a_{j 2}C_{j 2}\dots a_{jn}C_{jn}$


## Uses in triangular matrices 

To compute $\det \begin{bmatrix} a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\ 0 & a_{22} & a_{23} & \cdots & a_{2n} \\ 0 & 0 & a_{33} & \cdots & a_{3n} \\ \vdots & \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & 0 & \cdots & a_{nn} \end{bmatrix}$, we notice its upper triangular and as a result, can be easily calculated with cofactor expansion 

We first note that the first column, or the last row is the one with the largest number of zeroes, thus we start on that one. 

Note that $a_{21}\dots a_{n {1}}$ = 0


$$\begin{aligned}
&= a_{11} C_{11} + 0 + 0 + \cdots + 0 \\
&= a_{11} \cdot (-1)^{1+1} \det A_{11}
 = a_{11} \det \begin{bmatrix}
   a_{22} & & & \ast \\
   & a_{33} & & \\
   & & \ddots & \\
   0 & & & a_{nn}
 \end{bmatrix} \\
&= a_{11} a_{22} \det \begin{bmatrix}
   a_{33} & & & \ast \\
   & a_{44} & & \\
   & & \ddots & \\
   0 & & & a_{nn}
 \end{bmatrix} \\
&= a_{11} a_{22} a_{33} \cdots a_{nn}
\end{aligned}$$



We use the same trick again for not quite perfect triangular matrices 
$$
\begin{aligned} \det \begin{bmatrix} 2 & 2 & a & b \\ 1 & 3 & c & d \\ 0 & 0 & 3 & 4 \\ 0 & 0 & 1 & 1 \end{bmatrix} &= 2 \cdot C_{11} + 1 \cdot C_{21} \\ &= 2 \cdot (-1)^{1+1} \det A_{11} + 1 \cdot (-1)^{2+1} \det A_{21} \\ &= 2 \det \begin{bmatrix} 3 & c & d \\ 0 & 3 & 4 \\ 0 & 1 & 1 \end{bmatrix} - 1 \cdot \det \begin{bmatrix} 2 & a & b \\ 0 & 3 & 4 \\ 0 & 1 & 1 \end{bmatrix} \\ &= 2 \cdot 3 \cdot \det \begin{bmatrix} 3 & 4 \\ 1 & 1 \end{bmatrix} - 1 \cdot 2 \cdot \det \begin{bmatrix} 3 & 4 \\ 1 & 1 \end{bmatrix} \\ &= \det \begin{bmatrix} 2 & 2 \\ 1 & 3 \end{bmatrix} \cdot \det \begin{bmatrix} 3 & 4 \\ 1 & 1 \end{bmatrix} \end{aligned}$$
We can also use this concept for any column in a [[Matrix]], not just the ones on the edges. 
$$\begin{aligned} \det \begin{bmatrix} 1 & 1 & 0 & 2 \\ 2 & 0 & 0 & 3 \\ 3 & 2 & 1 & 4 \\ 4 & 3 & 0 & 5 \end{bmatrix} &= 1 \cdot C_{33} = 1 \cdot (-1)^{3+3} \det A_{33} \\ &= \det \begin{bmatrix} 1 & 1 & 2 \\ 2 & 0 & 3 \\ 4 & 3 & 5 \end{bmatrix} = \cdots \end{aligned}$$
Which can be simplified again using the middle row. 

