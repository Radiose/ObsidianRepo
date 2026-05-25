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



## Another method 
We define this definition as $\det[\vec{v}_{1}\vec{v_{2}}\dots \vec{v}_{3}]$   $(v_{1}\dots v_{2} \in \mathbb{R}^n)$ and form a **square matrix**
This is uniquely defined by the following [[Statement]]s

1: $\det [\vec{e}_{1}\vec{e}_{2}\dots\vec{e}_{n}]=1$ - this can be derived from thinking about unit squares/cubes 
2: the sign changes when you swap 2 columns of [[The determinant]]
3: $\det A$ is linear in every entry where you fix the other entries 
 - that is, $\det[v_{1},v_{w}+v_{v},\dots v_{n}]$ = $\det [\vec{v}_{1},\vec{v}_{2}\dots \vec{v}_{n}]$

Rule 2 in action 
$$\begin{aligned} & \det \begin{bmatrix} e & h & j & d \\ f & i & c & 0 \\ g & b & 0 & 0 \\ a & 0 & 0 & 0 \end{bmatrix} \xrightarrow{\text{swap col 1 and col 4}} \\ &= -\det \begin{bmatrix} d & h & j & e \\ 0 & i & c & f \\ 0 & b & 0 & g \\ 0 & 0 & 0 & a \end{bmatrix} \xrightarrow{\text{swap col 2 and col 3}} \\ &= (-1) \cdot (-1) \det \begin{bmatrix} d & j & h & e \\ 0 & c & i & f \\ 0 & 0 & b & g \\ 0 & 0 & 0 & a \end{bmatrix} \\ &= (-1) \cdot (-1) \cdot d \cdot c \cdot b \cdot a \end{aligned}$$
It also proves that [[Linearly dependent]] matrices have determinants of zero, as -x = x $\iff$ x=0
$$\begin{aligned}
\det \begin{bmatrix} a & e & a & i \\ b & f & b & j \\ c & g & c & k \\ d & h & d & l \end{bmatrix}
&\xrightarrow{\text{swap col 1 and col 3}}
(-1) \det \begin{bmatrix} a & e & a & i \\ b & f & b & j \\ c & g & c & k \\ d & h & d & l \end{bmatrix} \\
\Rightarrow \det A &= 0
\end{aligned}$$
