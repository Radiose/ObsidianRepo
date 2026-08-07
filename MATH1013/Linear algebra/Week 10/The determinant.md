---
aliases:
  - determinant
---
The determinant

# Leibniz definition 

Suppose A is some $n\times n$ matrix. Then, the determinant of $A$, denoted $\det(A)$ is defined by 
$\det (A)=\sum_{(m_{1},\dots ,m_{n})\in perm(n)}sign(m_{1},\dots m_{n})A_{m_{1},1},A_{m_{2},2}\dots A_{m_{n},n}$
This complex looking sum makes sense when the following is explained:
1: the index for the sum is each permutation, in the set of all possible permutations. 
2: The sign of a permutation is positive if an even number of swaps occurred, or negative if an odd number occurred.
3: The permutation can be thought of as a map from column to row. If a 3x3 matrix has permutation $(3,2,1)$, then this definition maps $(3,2,1)\to(1,2,3)$, where we have $A_{3,1}A_{2,2}A_{1,3}$


# Motivation for the determinant 

###  Decomposing the area of a parallelogram 
First we consider a parallelogram with area as shown below 
![[Pasted image 20260517130416.png]]
We demonstrate that the area is linear separate in $\vec{u} \ \vec{v}$

![[Pasted image 20260517130555.png]]

This diagram is FLAT DIAGRAM in $\mathbb{R}^2$, it only looks kind of like a rectangular prism. 
View $\vec{u}\  \vec{v}$, and then notice how u has been decomposed into u1 and u2. 
We aim to show that the area of uv, or OBCG = ADOG+ABCD 
This is easy, as the two triangles OAB and GDC are identical in area, so we can easily see how they take up the same area on the flat 2d plane. 

### Continuing to Area notation

If $\vec{x_{1}} ,\vec{x_{2}}\in \mathbb{R}^2$, then the area of the parallelogram [[span]]ned by them is denoted Area$(\vec{x_{1}},\vec{x_{2}})$ 

We derive the formula of Area$(\vec{x_{1}},\vec{x_{2}})$ with 2 basic facts 
1: the area of a rectangle with length A and width B is AB 
2: Area$(\vec{x_{1}},\vec{x_{2}})$ is linear in both factors 

How to prove 2:
Area$(\vec{u_{1}}+\vec{u_{2}},\vec{v})$  = Area$(\vec{u_{1}},\vec{v})$ + Area$(\vec{u_{2}},\vec{v})$
Area$(\vec{u},\vec{v_{1}}+\vec{v_{2}})$=  Area$(\vec{u},\vec{v_{1}})$+ Area$(\vec{u},\vec{v_{2}})$
 Area$(\vec{u},\lambda\vec{v})$  =  $\lambda$Area$(\vec{u},\vec{v})$
  Area$(\vec{\lambda u},\vec{v})$ = $\lambda$ Area$(\vec{u},\vec{v})$
The first two [[Statement]]s can be proven using the proof we utilised in decomposing parallelogram area 


The second two statements need to be proven in their own way
## proof of scalar areas 
This is a complex proof 
We first form a large parallelogram
![[Pasted image 20260517133041.png]]
let OA  = u, then OA' = $\lambda u$. For this case, we assume that $\lambda >1$ (similar proof for lambda $\le$ 1)
OB = v

We have to show that the area of OBC'A' = $\lambda \times$ the area of OBCA 
Note that the triangles OAC and ACA' have the same height 
$\frac{ACA'}{OAC}=\frac{AA'}{OA} \implies \frac{OCA'}{OAC}= \frac{OA'}{OA} = \lambda$
Note that in this diagram, Area(OBCA) = 2xArea(OAC) and OBC'A = 2xArea(OCA')
$\implies \frac{AREA(OBC'A')}{AREA(OBCA)}=\lambda$

### lambda < 0

We note that Area(U, V) means the area ![[Pasted image 20260517134550.png]]

Important notes: 
If $\vec{u} = 0, \vec{v} = 0$ or $\{ \vec{u} ,\vec{v} \}$ is [[Linearly dependent]] then Area($\vec{u}, \vec{v}$)=0

If$\{ \vec{u},\vec{v} \}$ is [[linearly independent]], then Area($\vec{v},\vec{u}$) is non zero. Whether its positive or negative depends on the following fact:
If we can rotate $\vec{u}$ by $0 \le \theta \le\pi$ and $\vec{u}$ is in the same direction as $\vec{v}$ after the rotation, then its positive, otherwise its negative. 

Now I cant be bothered to finish the proof, but follow the screenshot below

![[Pasted image 20260517134932.png]]

## Applying

Using all four statements established to prove point 2 above, we construct the folloing: 
![[Pasted image 20260517135136.png]]

Calculating each term: 
Area$(\begin{bmatrix}1 \\ 0\end{bmatrix},\begin{bmatrix}1, \\ 0\end{bmatrix})$ is a degenerate parallelogram with area 0 

Area$(\begin{bmatrix} 1  \\ 0\end{bmatrix},\begin{bmatrix}0 \\ 1\end{bmatrix})$ is = 1
Area$(\begin{bmatrix}0  \\ 1\end{bmatrix},\begin{bmatrix}1, \\ 0\end{bmatrix})$ gives an area of -1, using the signed area convention we established above 


Therefore, Area$(\begin{bmatrix} a \\ c\end{bmatrix},\begin{bmatrix}b \\ d\end{bmatrix})$ = ab $\cdot$ Area$(\begin{bmatrix}1 \\ 0\end{bmatrix},\begin{bmatrix}1  \\ 0\end{bmatrix})$ + ad Area$(\begin{bmatrix}1 \\ 0\end{bmatrix},\begin{bmatrix}0 \\ 1\end{bmatrix})$+cb Area$(\begin{bmatrix}0 \\ 1\end{bmatrix},\begin{bmatrix}1 \\ 0\end{bmatrix})$ + cd Area$(\begin{bmatrix}0 \\ 1\end{bmatrix},\begin{bmatrix}0 \\ 1\end{bmatrix})$



# Definition of [[The determinant]] for two dimensions
 for $\mathbb{R}^2: \det \begin{bmatrix}a \ b \\ c\ d\end{bmatrix}$ = ad-bc, using the motivation shown above 
 Some useful properties (based on the above proofs)  
 
 $\det \begin{bmatrix}a \ b \\ c\ d\end{bmatrix}$ $\not=0$ IFF the columns are [[linearly independent]].
  $\det \begin{bmatrix}a \ b \\ c\ d\end{bmatrix}$ = -  $\det \begin{bmatrix}b \ a \\ d\ c\end{bmatrix}$
 $\det \begin{bmatrix}a \ b \\ c\ d\end{bmatrix}$ = $\det \begin{bmatrix}a \ b \\ c\ d\end{bmatrix}^T$
$\det \begin{bmatrix}a \ b \\ c\ d\end{bmatrix} \not=0$ IFF the matrix is invertible  


## [[composition of Functions|composition]] of determinants 
If we have two 2x2 matrices A,B what is $det(AB)$ in terms of det(A) and Det(B)
![[Pasted image 20260517143303.png]]
we can represent Area$(T_{a}T_{b}(S_{1}))$ = $detA \times \det B \times Area(S)$. This is true for any S, so det(AB) = $det(A) \times \det(B)$


Also, $\det(A^{-1}) = \frac{1}{\det A}$ if A is an invertible [[Matrix]]


# Applications 

Find the area of a shape bound by a standard ellipse 


![[Pasted image 20260517143705.png]]
Basically, the magnitude of the ellipse times the unit circle gives the answer. This is because the ellipse is symmetrical. 



# Three dimensions 
Find the volume of a parallelepiped spanned by three vectors in $\mathbb{R}^3$
Let vol($\vec{u},\vec{v},\vec{w}$) denote the oriented volume of the parallelepiped spanned by the three vectors 

From the same intuition from 2d, vol($\vec{u},\vec{v},\vec{w}$) should satisfy 5 rules 
1: vol($\vec{u_{1}}+\vec{u}_{2},\vec{v},\vec{w}$ = vol($\vec{u_{1}},\vec{v},\vec{w}$) + vol($\vec{u_{2}},\vec{v},\vec{w}$) and similarly for the other vectors 
2: vol($\lambda\vec{u},\vec{v},\vec{w}$) = $\lambda$vol($\vec{u},\vec{v},\vec{w}$) for any $\lambda \in \mathbb{R}$, and similarly for the other two vectors
3: Swapping any vectors should change the sign, so vol($\vec{u},\vec{v},\vec{w}$) = - vol($\vec{u},\vec{w},\vec{v}$)
4: vol($\begin{bmatrix}1  \\ 0 \\ 0\end{bmatrix},\begin{bmatrix}0  \\ 1  \\ 0\end{bmatrix},\begin{bmatrix}0  \\ 0  \\ 1\end{bmatrix}$) should be 1, the unit cube 
5vol($\vec{u},\vec{v},\vec{w}$) = 0  $\iff\{ \vec{u}, \vec{v}, \vec{w} \}$ is a linearly dependent set of vectors 

Now we apply these rules ![[Pasted image 20260518165702.png]]
![[Pasted image 20260518165728.png]]
Remove linearly dependent sets 
![[Pasted image 20260518165757.png]]

![[Pasted image 20260518165833.png]]

Now apply rules 2, 3 and 4 
![[Pasted image 20260518165900.png]]

This leaves us with the final equation 

$\det \begin{bmatrix}a_{11} \ a_{12} \ a_{13}  \\ a_{21} \ a_{22} \ a_{23}  \\ a_{31} \ a_{32} \ a_{33}\end{bmatrix}$ = $a_{11}a_{22}a_{33}-a_{11}a_{23}a_{32}-a_{12}a_{21}a_{33}+a_{13}a_{21}a_{32}+a_{12}a_{23}a_{31}-a_{13}a_{22}a_{31}$

we group these into terms 
$a_{11}(a_{22}a_{33}-a_{23}a_{32})$
$-a_{12}(a_{21}a_{33}-a_{23}a_{31})$
$+a_{13}(a_{21}a_{32}-a_{22}a_{31})$
we use mathematical [[Induction]] to cook up a formula 


 ![[cofactor expansion]]



