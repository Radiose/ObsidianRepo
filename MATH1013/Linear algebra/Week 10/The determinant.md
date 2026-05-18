The determinant

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

If $\vec{x_{1}} ,\vec{x_{2}}\in \mathbb{R}^2$, then the area of the parallelogram [[Span]]ned by them is denoted Area$(\vec{x_{1}},\vec{x_{2}})$ 

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



# Definition of [[The determinant]]
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