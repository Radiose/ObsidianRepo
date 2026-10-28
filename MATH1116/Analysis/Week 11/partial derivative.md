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