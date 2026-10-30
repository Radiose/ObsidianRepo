---
aliases:
---
# The partial derivative
![[partial derivative]]
# Motivation
## Remark 
Consider $$f:\mathbb{R}^2 \to \mathbb{R} \\ (x,y) \mapsto \frac{xy}{x^2+y^2}$$Recall $f$ is not [[continuous function|continuous]] at $0$, but $$\lim_{ h \to 0 }\frac{f(h,0)-f(0,0)}{h}=0\\ \\ \lim_{ h \to 0 }\frac{f(0,h)-f(0,0)}{h}=0$$So both [[partial derivative]]s exist, and even agree, but this obviously does not imply continuity.
For this reason, we need a new definition of differentiable, that is deeper than just "the derivative exists".

# Definition 
Let $f:B(C,R) \to \mathbb{R}$. We say $f$ is differentiable at $x \in B(C,R)$ if there exists some $T:\mathbb{R}^n \to\mathbb{R}$ that is a [[linear map]], there exists some $\epsilon :\mathbb{R}^n \to \mathbb{R}$ such that $\lim_{ x \to y }\epsilon(y-x)=0$ such that for all $y \in \mathbb{R}^n$, $f(y)=f(x)+T(y-x)+ \lVert y-x \rVert \epsilon \lVert y-x \rVert$.

Note the similarity of this to [[Taylors theorem]]. In single variable calculus, $T(y-x)$ is the first derivative of $f(x)$.

Recall [[derivative|differentiability for single variable dimensions]]. In that case, we are saying that the value of $f(x)$ can be well approximated by a line. The same idea applies for higher dimensions. 
The graph of $y \mapsto f(x)+T(y-x)$ is a hyperplane, tangent to the graph of $y \mapsto f(y)$ at $x$.
Think about the visual representation for [[Taylors theorem]]. In particular, the centered point.

# Theorem 
Let $f:B(C,R) \to \mathbb{R}$ be differentiable at $x \in B(C,R)$.
Then, it is [[multivariate continuity|continuous]] at $x$.
### Proof 
We have that $\exists T:\mathbb{R}^n \to \mathbb{R}$ linear, $\exists \epsilon: \mathbb{R}^n \to \mathbb{R}$ 
This implies that $\forall y\in B(C,R):\quad f(y)=f(x)+T(y-x)+ \lVert y-x \rVert\epsilon(y-x)$
$T$ is represented by a $1\times n$ matrix $(a_{1},\dots,a_{n})$

$\implies T(y-x)=(a_{1},\dots,a_{n})\cdot \begin{pmatrix}y_{1}-x_{1}  \\  . \\  . \\  . \\  y_{n}-x_{n}\end{pmatrix}$
Thus, $T(y-x) \leq \lVert (a_{1},\dots,a_{n}) \rVert \ \lVert y-x \rVert$ via CS 
$\implies T(y-x) \xrightarrow[y \to x]{}0$
