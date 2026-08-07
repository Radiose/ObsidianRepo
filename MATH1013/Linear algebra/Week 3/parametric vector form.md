---
{}
---
parametric vector form
You can use this concept of [[linearity]] to create something called a parametric [[vector]] form
This is necessary when you have a free variable present in your solution. As with any [[Consistent linear system]] that has infinite solutions, you will write all equations in terms of the free variable.

For example $\begin{matrix}[2 \ 4]  \\  [4 \ 8]\end{matrix} \begin{pmatrix}x_{1} \\ x_{2}\end{pmatrix} = \begin{pmatrix}2 \\ 4 \end{pmatrix}$
solving this augmented [[Matrix]] gives $\begin{matrix}[1 & 2 & 1] \\ [0 & 0 & 0]\end{matrix}$. this make x2 a free variable. Therefore, $\begin{pmatrix}x_{1} \\ x_{2}\end{pmatrix}=\begin{pmatrix}1 \\ 0\end{pmatrix}+t\begin{pmatrix}-2  \\ 1\end{pmatrix}$. This is telling us that to get to x1,x2, we start at 1,0 and move -2 and 1 times t units. 


This is very useful for determining things about linear equations

take the singular equation $x_{2}+3x_{3}=1$ and solve it. (original question is find the [[parametric vector form]] of the plane in $\mathbb{R}^3$)
Putting this in a matrix yields $\begin{matrix}[0 & 1 & 3 & | & 1]\end{matrix}$
As we can see, x2 is a pivot, making x1 and x3 free variables. 
Therefore, we can write x2 in terms of x3 (x1 is harder as it has 0 as a coefficient)
$x_{2}=1-3x_{3}$. Remember that $x_{1},x_{3}$ are any real number

putting the solutions into a vector yields the solution [[set]] $\{  \begin{pmatrix}x_{1}  \\  1-3x_{3}  \\ x_{3}\end{pmatrix}|x_{1},x_{3} \in \mathbb{R}\}$. Now simplifying this into [[parametric vector form]], we get $\{\begin{pmatrix}0  \\  1 \\ 0 \end{pmatrix} + x_{1}\begin{pmatrix}1 \\ 0 \\ 0\end{pmatrix} +x_{2}\begin{pmatrix}0 \\ -3 \\ 1\end{pmatrix}|x_{1},x_{2} \in \mathbb{R}\}$. So the plane in $\mathbb{R}^3$ are any vectors in this format. 

Remember that for an equation to [[span]] a plane in $\mathbb{R}^3$, there must 2 free variables. If theres one, it spans only a line. 
![[Pasted image 20260311121702.png]]

This image may aid in geometrically understanding the solution [[set]]




Another example
recall that a solution to a system of linear equations will provide you with the intersection point of a line. 
Recall that 2 planes that are not parallel intersect at a line. 
when do
$x_{2}+3x_{3}=1$ and $x_{1}+x_{2}+x_{3}=0$ intersect
get RREF$\begin{matrix}[1 & 0 & -2 & | & -1]  \\  [0  & 1 & 3 & | & 1] \end{matrix}$
this gives us x3 as a free variable. One free variable means that the solution is a line in $\mathbb{R}^3$
writing as a [[parametric vector form]]
, the solution set is all vectors in the form $\begin{pmatrix}-1  \\  1  \\  0\end{pmatrix}+x_{3}\begin{pmatrix}2  \\  3  \\  -1\end{pmatrix}$ | $x_{3}\in \mathbb{R}$. This is basically just saying start at the point in the first vector, then move this way in the magnitude of x3.



using [[parametric vector form]] to take a line through 2 points. 

two points (8,-5,4) and (6,3,2)
getting the line between them requires getting the [[Position vector]]s difference between them.
$\begin{pmatrix}8  \\ -5  \\ 4\end{pmatrix}-\begin{pmatrix}6 \\ 3 \\ 2\end{pmatrix}$ = $\begin{pmatrix}2  \\ -8  \\ 2\end{pmatrix}$
for a [[Position vector]] p we can take the position vector of either point and use it to create a [[parametric vector form]] where x is the position on the line. 
$\vec{x}=\begin{pmatrix}8  \\  -5  \\  4\end{pmatrix}+t \begin{pmatrix}2  \\  -8  \\ 2\end{pmatrix}$ 




Find a [[parametric vector form]] to find the plane through 3 points 
P(1,-1,2)  Q(-1,-1,6) R(-1,1,4)

The [[Position vector]] QP is P - Q or $\begin{pmatrix}1 \\ -1 \\ 2\end{pmatrix}-\begin{pmatrix}-1  \\  -1  \\ 6\end{pmatrix}$ = $\begin{pmatrix}2  \\ 0  \\ -4\end{pmatrix}$ 
QR = $\begin{pmatrix} -1  \\ 1 \\ 4\end{pmatrix}-\begin{pmatrix} -1  \\ -1  \\ 6\end{pmatrix} = \begin{pmatrix}0 \\ 2 \\ -2 \\ \end{pmatrix}$ 

Therefore, the [[parametric vector form]] of the plane that passes through these two points, is $\begin{pmatrix}-1 \\ -1 \\ 6\end{pmatrix}+x_{1}\begin{pmatrix}2 \\ 0  \\ -4\end{pmatrix}+ x_{2}\begin{pmatrix}0 \\ 2 \\ -2\end{pmatrix}$
NOTE: you could do this any other way, having R as the constants and RP as one vector and RQ as the other one. 