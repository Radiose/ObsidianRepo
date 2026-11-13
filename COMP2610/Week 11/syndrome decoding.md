given $\mathbf{r}=r_{1},\dots,r_{7}$ assume a binary [[symmetric channel]] with small noise level $f$.


we define the **syndrome** as the length 3 vector $\mathbf{z}$ that describes the pattern of violations of the parity bits $r_{5},r_{6},r_{7}$. In particular $\mathbf{z}_{i}=1$ when the $i$th parity bit does not match the parity of $\mathbf{r}$.
Note that flipping a single bit leads to a different syndrome.

We check parity bits $r_{5},r_{6},r_{7}$ and identify the syndrome.
Then, we unflip the single bit responsible for this patter of violation. 

we have $\mathbf{z}=\mathbf{Hr}$ where $\mathbf{H}=\begin{bmatrix} \mathbf{P} & \mathbf{I}_{3}\end{bmatrix}$ = $\begin{bmatrix} 1 & 1 & 1 & 0 & 1 & 0 & 0 \\  0 & 1 & 1 & 1 & 0 & 1 & 0 \\  1 & 0 & 1 & 1 & 0 & 0 & 1\end{bmatrix}$

View file:///C:/Users/henry/Downloads/L21%20(2).pdf slides 39 for more. 

