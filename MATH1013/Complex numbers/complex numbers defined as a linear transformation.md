

We first aim to show that every [[Complex number]] $z=x+yi$ is in the $\mathbb{R}$ linear [[Span]] of 1 and i

That is, $Span_{\mathbb{R}}\{ 1,i \}=\{ x_{1}\times_{1} + x_{2}i | x_{1},x_{2} \in \mathbb{R} \} = \mathbb{C}$


# Proof of [[linearly independent |linear independence]]
To demonstrate this rigorously, we have to show that 1 and $i$ are $\mathbb{R}$ [[linearly independent]]
We prove this through the following [[Statement]]:
If there is a [[Linear combination of vectors]] $a \times 1 + B \times i =0$ ($a,b \in \mathbb{R}$), we have to show that $a = b = 0$
This proof relies on the fact that $i^2 = -1$
if $b = 0, \ a+bi = 0 \implies a =0$ so proven 

if $b \not=0,\ a+bi =0 \implies bi =-a$
$\implies i = -\frac{a}{b}$
$\implies \frac{a^2}{b^2}=-1$
thus, a [[proof by contradiction]] as $a,b \in \mathbb{R}$


## Multiplication as [[Linear transformation]]s
We now view multiplication of [[Complex number]]s as a linear transformation on $\mathbb{R}^2$ with the following rules 
$z \in \mathbb{C}$, $z: \mathbb{C} \to \mathbb{C}$
	$z_{1} \mapsto zz_{1}$
We convert this to linear transformation 
$z:\mathbb{R}^2 \to \mathbb{R}^2$ via the proof we demonstrated above as well as the coming proof of [[linearity]]

## Proof of [[linearity]]
$z(az_{1})=az(z_{1})$ for any $a \in \mathbb{R}$
$z(z_{1}+z_{1})=z(z_{1})+z(z_{2})$
These are both checkable manually, 

$\mathbb{C}$ as a 2 dimensional [[vector]] space has a basis $\mathcal{B}= \{1,i  )$

## The standard matrix
We find the [[Standard Matrix]] of $z$
Recall that the [[Standard Matrix]] is given by $[T(\vec{e_{1}}),T(\vec{e_{2}})]$
The coordinate of $x+yi$ under basis $\mathcal{B}=\{1,i)$
$x+yi = 1x+yi \implies [x+yi]_{B}= \begin{bmatrix} x  \\  y\end{bmatrix}$
if $T = z: \mathbb{R}^2 \to \mathbb{R}^2$
$\vec{e}_{1} = \begin{bmatrix}1  \\ 0\end{bmatrix}$ and $\vec{e_{2}} = \begin{bmatrix}0 \\ i\end{bmatrix}$

Suppose $z = x+yi\ \ \ (x,y\in \mathbb{R})$
$z(\vec{e}_{1})=z*1=z$
$\implies [z(\vec{e}_{1})]_{B}=\begin{bmatrix} x \\ y\end{bmatrix}$
$z(\vec{e_{2}}) = z $