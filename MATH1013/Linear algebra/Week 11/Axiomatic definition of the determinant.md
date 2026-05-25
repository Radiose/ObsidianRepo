## Another method 
We define this definition as $\det[\vec{v}_{1}\vec{v_{2}}\dots \vec{v}_{3}]$   $(v_{1}\dots v_{2} \in \mathbb{R}^n$ and form a **square matrix**)
This is uniquely defined by the following [[Statement]]s

1: $\det [\vec{e}_{1}\vec{e}_{2}\dots\vec{e}_{n}]=1$ - this can be derived from thinking about unit squares/cubes 
2: the sign changes when you swap 2 columns of [[The determinant]]
3: $\det A$ is linear in every entry where you fix the other entries 
 - that is, $\det[v_{1},v_{w}+v_{v},\dots v_{n}]$ = $\det [\vec{v}_{1},\vec{v}_{2}\dots \vec{v}_{n}]$

### Rule 2 in action 
$$\begin{aligned} & \det \begin{bmatrix} e & h & j & d \\ f & i & c & 0 \\ g & b & 0 & 0 \\ a & 0 & 0 & 0 \end{bmatrix} \xrightarrow{\text{swap col 1 and col 4}} \\ &= -\det \begin{bmatrix} d & h & j & e \\ 0 & i & c & f \\ 0 & b & 0 & g \\ 0 & 0 & 0 & a \end{bmatrix} \xrightarrow{\text{swap col 2 and col 3}} \\ &= (-1) \cdot (-1) \det \begin{bmatrix} d & j & h & e \\ 0 & c & i & f \\ 0 & 0 & b & g \\ 0 & 0 & 0 & a \end{bmatrix} \\ &= (-1) \cdot (-1) \cdot d \cdot c \cdot b \cdot a \end{aligned}$$
It also proves that [[Linearly dependent]] matrices have determinants of zero, as -x = x $\iff$ x=0
$$\begin{aligned}
\det \begin{bmatrix} a & e & a & i \\ b & f & b & j \\ c & g & c & k \\ d & h & d & l \end{bmatrix}
&\xrightarrow{\text{swap col 1 and col 3}}
(-1) \det \begin{bmatrix} a & e & a & i \\ b & f & b & j \\ c & g & c & k \\ d & h & d & l \end{bmatrix} \\
\Rightarrow \det A &= 0
\end{aligned}$$

### Rule 3 in action 

$$\begin{aligned}
& \det \begin{bmatrix} a_{11} & a_{12}+b_{12} & a_{13}+b_{13} \\ a_{21} & a_{22}+b_{22} & a_{23}+b_{23} \\ a_{31} & a_{32}+b_{32} & a_{33}+b_{33} \end{bmatrix} \\[10pt]
&\overset{\substack{\text{linear in col 2}\\ \text{fix col 1, col 3}}}{=}
\det \begin{bmatrix} a_{11} & a_{12} & a_{13}+b_{13} \\ a_{21} & a_{22} & a_{23}+b_{23} \\ a_{31} & a_{32} & a_{33}+b_{33} \end{bmatrix}
+ \det \begin{bmatrix} a_{11} & b_{12} & a_{13}+b_{13} \\ a_{21} & b_{22} & a_{23}+b_{23} \\ a_{31} & b_{32} & a_{33}+b_{33} \end{bmatrix} \\[10pt]
&\overset{\substack{\text{fix col 1, col 2}\\ \text{linear in col 3}}}{=}
\det \begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{bmatrix}
+ \det \begin{bmatrix} a_{11} & a_{12} & b_{13} \\ a_{21} & a_{22} & b_{23} \\ a_{31} & a_{32} & b_{33} \end{bmatrix} \\[6pt]
&\qquad + \det \begin{bmatrix} a_{11} & b_{12} & a_{13} \\ a_{21} & b_{22} & a_{23} \\ a_{31} & b_{32} & a_{33} \end{bmatrix}
+ \det \begin{bmatrix} a_{11} & b_{12} & b_{13} \\ a_{21} & b_{22} & b_{23} \\ a_{31} & b_{32} & b_{33} \end{bmatrix}
\end{aligned}$$
This is important, as you can only fix **one** column at a time. 
