homogenous coordinates 
rotation by a fixed coordinate is not defined as a [[Linear transformation of R n]], this is because $T(\vec{0}) \not= \vec{0}$
Instead, we utilise a trick to convert a [[rotation transformation]] into a [[Linear transformation of R n]] by taking the [[vector]] into a higher dimensional space. Similar problems also occur during translation transformations. 

This is done by making the nth entry in a vector 1 when converting from $\mathbb{R}^{n-1} \to \mathbb{R}^n$, so $\begin{bmatrix} 2 \\  5\end{bmatrix} \to \begin{bmatrix} 2 \\ 5 \\ 1\end{bmatrix}$
Then plugging this in a rotation matrix:
For rotations, the matrix is almost unchanged 
$\begin{bmatrix}\cos \theta, -\sin \theta, 0 \\\sin \theta, \ \ \cos \theta, 0  \\ \ \ \  0 \ \ \ \ \  \ \ \ \ \ \ \ \ 0\ \ \ \ \ \ \ \ 1 \end{bmatrix}$


You can also plug this into a translation matrix that looks like below to make translation linear 
$\begin{bmatrix}x +\alpha  \\ y+\beta \\ 1\end{bmatrix} = \begin{bmatrix}1 \ 0\ \alpha \\ 0\ 1\ \beta  \\  0\ 0\ 1\end{bmatrix}\begin{bmatrix} x  \\  y  \\ 1\end{bmatrix}$
Note that even if you input the original [[vector]] with a  third coordinate thats not 1, it will scale the translation 
$\begin{bmatrix}x  \\ y \\ 2\end{bmatrix}$ will output $\begin{bmatrix}x + 2\alpha  \\ y+2\beta \\ 2\end{bmatrix}$

Also note that $\begin{bmatrix}3 \\ 4 \\ 5\end{bmatrix} = \begin{bmatrix}  \frac{3}{5} \\ \frac{4}{5} \\ 1\end{bmatrix}$ and both represent the same point and have the same x y coordinates