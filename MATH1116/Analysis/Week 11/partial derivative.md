Let $f:B(C,R)\to \mathbb{R}$
If $$\lim_{ h \to 0 }\frac{f(x+hv)-f(x)}{h} =: \frac{\partial f}{\partial v}(x)$$exists, we say that $f$ admits a partial [[derivative]] in the direction of $v$.

# Definition WRT the CB 
Let $f:B(C,R) \to \mathbb{R}$
Let $e_{j}$ be a [[canonical basis]] for $j =  1,2,\dots,n$
If $f$ admits a partial derivative in the direction of $e_{j}$, we write $$  f_{j}(x);= fx_{j}(x) := \frac{\partial f(x)}{\partial x_{j}} := \frac{\partial f}{\partial e_{j}}(x)$$
## Remark 
Note that when we differentiate with respect to a canonical basis function, what we are doing is fixing other variables as constants. 
This is illustrated below 
#### Example 
Let $f:\mathbb{R}^2 \to \mathbb{R}\\ \quad \ x,y \mapsto xy^2+y$
Consider $g:\mathbb{R} \to \mathbb{R}\\ \quad \quad x \mapsto f(x,y)$
$g'(x)=y^2\quad\forall x \in \mathbb{R}$
$\frac{\partial f}{\partial x}= \lim_{ h \to 0 } \frac{1}{h} \left( \left[ (x+h)y^2+y \right]-(xy^2+y) \right)$
$= \lim_{ h \to 0 }y^2 =y^2$

# Properties of partial derivatives  
## Linearity property 
$$\frac{ \partial \lambda f+g }{ \partial v }=\frac{ \partial \lambda f }{ \partial v }+ \frac{ \partial g }{ \partial v }$$
## The [[product rule]]
$\frac{ \partial f \cdot g }{ \partial v }= \frac{ \partial f }{ \partial v } \cdot g + \frac{ \partial g }{ \partial v }+f$

### Proofs 
exercise



## Higher order partial derivatives 
Let $f:\mathbb{R}^n \to\mathbb{R}$ , $j,k \in \{ 1,\dots,n \}$
Assume $f_{x_{j}}$  admits a partial derivative. 
We write $$\frac{ \partial^2 f }{ \partial x_{k} \partial x_{j} } $$ for the partial derivative of order 2. 

![[Laplacian operator]] 

# Theorem 
Let $f:\mathbb{R}^2 \to \mathbb{R}$  and $(x_{0},y_{0})\in \mathbb{R}^2$
Assume that $f$ admits a partial derivative of order 2, $\frac{ \partial ^2f }{ \partial x^2 },\frac{ \partial ^2f }{ \partial y^2 },\frac{ \partial ^2 f }{ \partial x\partial y }$ in $B((x_{0},y_{0}),R)$ with positive R. 
Assume that $\frac{ \partial ^2 f }{ \partial x \partial y  }$ is [[multivariate continuity|continuous]] on $B((x_{0},y_{0}),R)$, then 
$\frac{ \partial ^2 f }{ \partial x \partial y}$ exists, and is equal to $\frac{ \partial ^2 f }{ \partial y \partial x }$

### Proof 
Let $(x_{0},y_{0}) \in B(C,R)$. let $\epsilon >0$.
Pick $\delta$ : $\forall(x,y)\in B(C,R)$, $$\lVert (x,y)-(x_{0},y_{0}) \rVert <\delta \implies \left\lvert  \frac{ \partial ^2 f }{ \partial x \partial y } (x,y) - \frac{ \partial ^2 f }{ \partial x \partial y }(x_{0},y_{0})    \right\rvert<\epsilon $$
Define $$g:\left( \frac{-\delta}{\sqrt{ 2 }}, \frac{\delta}{\sqrt{ 2 }} \right)^2 \to \mathbb{R} \\ \\ (h,k) \mapsto f(x_{0}+h,y_{0}+k)-f(x_{0}+h,y_{0})-f(x_{0},y_{0}+k)+f(x_{0},y_{0})$$
The motivation for this is that we are trying to compute the second derivative. We exploit the continuity of the mixed first derivatives.

Fix $(h,k) \in \left(  -\frac{\delta}{\sqrt{ 2 }}, \frac{\delta}{\sqrt{ 2 }} \right)^2$
Consider $G: \left( \frac{-\delta}{\sqrt{  2}}, \frac{\delta}{\sqrt{ 2 }} \right) \to \mathbb{R}$, with $(k)\mapsto g(h,k)$
Via the mean value theorem, $\exists \theta(k) \in \left[ y_{0},y_{0}+k \right]$ such that $G(k)-G(0)=G'(\theta (k))\cdot k$
IE $$g(h,k)- \left[ f(x_{0}+h,y_{0}+k)-f(x_{0}+h,y_{0})-f(x_{0},y_{0}+k)+f(x_{0},y_{0})  \right] \\ \\ = \left[  \frac{ \partial f }{ \partial y }(x_{0}+h,\theta(k))-\frac{ \partial f }{ \partial y } (x_{0}+h,\theta(k))  \right] $$
