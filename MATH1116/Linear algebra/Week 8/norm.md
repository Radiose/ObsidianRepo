---
aliases:
  - normed space
---
A norm of a [[vector]] is defined typically defined in relation to an [[inner product]].
A norm on a [[vector space]] $V$ has the following properties:
(1) $\lVert \mathbf{v} \rVert\geq 0\quad \forall \mathbf{v}\in V$
(2) $\lVert \mathbf{v} \rVert=\mathbf{0}\iff \mathbf{v=0}$
(3) $\lVert \lambda \mathbf{v} \rVert= \lvert \lambda \rvert \lVert \mathbf{v} \rVert\quad \forall \lambda \in \mathbb{F},\ \ \forall v\in V$
(4) $\lVert \mathbf{v+u} \rVert\leq \lVert \mathbf{v} \rVert+\lVert \mathbf{u} \rVert$
(5) $\lVert \mathbf{u} \rVert=\sqrt{ \langle \mathbf{u},\mathbf{v} \rangle }$

## Normed space 
A normed space is a [[vector space]] $V$ along with a norm. 



# Theorem (Pythagorean)
If $\mathbf{v},\mathbf{w}$ are [[orthogonal vectors|orthogonal]], $\lVert \mathbf{u}+\mathbf{w} \rVert^2=\lVert \mathbf{u} \rVert^2+\lVert \mathbf{v} \rVert^2$

 ![InkDrawing](<attachments/Ink/Drawing/2026.10.2 - 19.05pm.svg>) [Edit Drawing](https://youtu.be/2arL1jh8ihA?type=inkDrawing&width=500&aspectRatio=1.778&viewBoxX=0&viewBoxY=0&viewBoxW=2000&viewBoxH=1125)
### Proof 
$\lVert \mathbf{v}+\mathbf{w} \rVert^2=\langle \mathbf{v+w},\mathbf{v+w} \rangle=\langle \mathbf{v,v} \rangle+\langle \mathbf{v,w} \rangle+\langle \mathbf{w,v} \rangle+\langle \mathbf{w,w} \rangle$
$$=\lVert \mathbf{v} \rVert ^2+\mathbf{\lVert w \rVert }^2$$

# Cauchy Schwarz inequality
![[Cauchy-schwarz inequality]]


# Remark 
Not every normed space necessarily comes from an [[inner product space]].



# Remark 
Note that $\lVert \mathbf{v} \rVert=\sqrt{ \langle \mathbf{v,v} \rangle }$ defines an norm over an [[inner product space]].
# Lemma 
If $V$ is an [[inner product space]], then $\forall \mathbf{u,v}\in V$, $2(\lVert \mathbf{u} \rVert^2+\lVert  \mathbf{v}\rVert^2)=\lVert \mathbf{u+v} \rVert^2+\lVert \mathbf{u-v} \rVert^2$
### Proof 
RHS = $\langle \mathbf{u+v},\mathbf{u+v} \rangle+\langle \mathbf{u-v}, \mathbf{u-v} \rangle$ (via the above remark)
$=\langle \mathbf{u,u} \rangle+\langle  \mathbf{u,v}\rangle+\langle \mathbf{v,u} \rangle+\langle \mathbf{v,v} \rangle+\langle \mathbf{u,u} \rangle-\langle \mathbf{u,v} \rangle-\langle \mathbf{v,u} \rangle+\langle \mathbf{v,v} \rangle$
$=2 \lVert \mathbf{u} \rVert^2+2 \lVert \mathbf{v} \rVert^2=LHS \blacksquare$


#### Examples
Consider the following examples:
$(1)$: Let $V=C([0,1],\mathbb{F})$
Define p-norm  $\lVert \mathbb{F} \rVert_{p}=\left( \int_{0}^1 \lvert f(x) \rvert^pdx \right)^{1/p}$
If $p=\infty$, $\lVert \mathbb{F} \rVert_{\infty}=\sup\{ f(x)|x \in[0,1] \}$

We show that the sup norm doesn't obey the lemma above. 
Let $f(x)=x,\quad g(x)=1-x$ ( over $[0,1]$)
$2\left( \lVert f \rVert_{\infty}^{2} + \lVert g \rVert_{\infty}^2\right)=2(1+1)=4$
$\lVert (f+g) (x)\rVert_{\infty}=1$
$\lVert (f-g)(x) \rVert_{\infty}=1$
$1+1 \not=4$ 

$(2)$
$V=\mathbb{F}^n$
$\lVert \begin{bmatrix} u_{1}   \\  . \\  u_{n}\end{bmatrix} \rVert_{p}=\left( \mathbf{u}_{1}^p+\dots+\mathbf{u}_{n}^p \right)^{1/p}$ 
