---
aliases:
  - elementary matrices
---
 Elementary [[Matrix]]
The key idea surrounding an elementary [[Matrix]] is that *every* [[Row operation]] corresponds with an elementary matrix.

The three key row operations can be expressed as elementary matrices. Note that for each of these, the row dimension is the only important dimension to creating an elementary matrix (ROW operation). 

# Operation 1:
$R_{i} \to c \cdot R_{i}$ 
This can be expressed through changing the ith rows identity input to $c$
EG $R_{3} \to 3 R_{3}$ where R is a row of a 4xn matrix 
$\begin{bmatrix}1000  \\ 0100  \\ 00c0  \\ 0001\end{bmatrix}$


# Operation 2
Swapping rows 
$R_{i} \leftrightarrow R_{j}$ is denoted as swapping the ith and jth rows.
This is done by moving the identity entries of the ith from the ith column to the jth, and the jth row moving from the jth column to the ith column. 
For example, $R_{2} \leftrightarrow R_{4}$, where R is a row of an 5$\times$n matrix   
$\begin{bmatrix}1 0 0 0 0\\00010 \\ 00100  \\ 01000  \\ 00001\end{bmatrix}$ 

# Operation 3
Addition of rows
$R_{i} \to R_{i}+cR_{j}$

$\begin{bmatrix}a_{11}a_{12} \\ a_{21} a_{22}  \\ a_{31} a_{32}\end{bmatrix} \to \begin{bmatrix}a_{11}+ca_{31} a_{12}+c_{32}  \\ a_{21} a_{22}  \\ a_{31} a_{32}\end{bmatrix}$  is expressed as 
$\begin{bmatrix}1 0c  \\ 0 10 \\ 001\end{bmatrix} \begin{bmatrix}a_{11}a_{12} \\ a_{21} a_{22}  \\ a_{31} a_{32}\end{bmatrix}$
An easy way to think about this is what row are we doing it to, and what row is doing it? The row that we are doing it to is the row in the elementary matrix, while the row that is doing it is the column number. 