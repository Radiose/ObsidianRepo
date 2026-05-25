[[The determinant|determinant]] of an [[Inverse matrix]]
We note first that $\det A \not=0 \iff A$ is invertible 
$AA^{-1}=I_{n}$, we expand this to 
$$
A = \begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & & & \vdots \\
\vdots & & & \vdots \\
a_{n1} & \cdots & & a_{nn}
\end{bmatrix}
\qquad
A^{-1} = \begin{bmatrix}
M_{11} & M_{12} & \cdots & M_{1n} \\
M_{21} & & & \vdots \\
\vdots & & & \vdots \\
M_{n1} & \cdots & & M_{nn}
\end{bmatrix}$$
$$\begin{aligned}
& \bullet\ a_{11} M_{11} + a_{12} M_{21} + \cdots + a_{1n} M_{n1} = 1 \text{ based off the definition of matrix multiplication}\\
& \quad (a_{11} C_{11} + a_{12} C_{12} + \cdots + a_{1n} C_{1n}) = \det A \neq 0 \\
\text{we can divide now}& \quad M_{11} = \frac{C_{11}}{\det A}, \quad M_{21} = \frac{C_{12}}{\det A}, \quad \cdots \quad M_{n1} = \frac{C_{1n}}{\det A} \\[6pt]
& \bullet\ a_{21} M_{12} + a_{22} M_{22} + a_{23} M_{32} + \cdots + a_{2n} M_{n2} = 1 \\
& \quad \Rightarrow M_{12} = \frac{C_{21}}{\det A}, \quad M_{22} = \frac{C_{22}}{\det A}, \quad \cdots \quad M_{n2} = \frac{C_{2n}}{\det A}
\end{aligned}$$


We notice a pattern, and as such define a [[theorem]]

$(A^{-1})_{ij} = M_{ij} = \frac{C_{ji}}{\det A}= (-1)^{i+j}\det \frac{A_{ji}}{\det A}$



