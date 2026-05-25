
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

What we aim to do is to generalise this 
$\det \begin{bmatrix}a_{11}a_{21}\end{bmatrix}$