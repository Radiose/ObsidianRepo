A norm of a [[vector]] is defined in relation to an [[inner product]].
A norm on a [[vector space]] $V$ has the following properties:
(1) $\lVert \mathbf{v} \rVert\geq 0\quad \forall \mathbf{v}\in V$
(2) $\lVert \mathbf{v} \rVert=\mathbf{0}\iff \mathbf{v=0}$
(3) $\lVert \lambda \mathbf{v} \rVert= \lvert \lambda \rvert \lVert \mathbf{v} \rVert\quad \forall \lambda \in \mathbb{F},\ \ \forall v\in V$
(4) $\lVert \mathbf{v+u} \rVert\leq \lVert \mathbf{v} \rVert+\lVert \mathbf{u} \rVert$
(5) $\lVert \mathbf{u} \rVert=\sqrt{ \langle \mathbf{u},\mathbf{v} \rangle }$





# Theorem (Pythagorean)
If $\mathbf{v},\mathbf{w}$ are [[orthogonal vectors|orthogonal]], $\lVert \mathbf{u}+\mathbf{w} \rVert^2=\lVert \mathbf{u} \rVert^2+\lVert \mathbf{v} \rVert^2$

 ![InkDrawing](<attachments/Ink/Drawing/2026.10.2 - 19.05pm.svg>) [Edit Drawing](https://youtu.be/2arL1jh8ihA?type=inkDrawing&width=500&aspectRatio=1.778&viewBoxX=0&viewBoxY=0&viewBoxW=2000&viewBoxH=1125)
### Proof 
$\lVert \mathbf{v}+\mathbf{w} \rVert^2=\langle \mathbf{v+w},\mathbf{v+w} \rangle=\langle \mathbf{v,v} \rangle+\langle \mathbf{v,w} \rangle+\langle \mathbf{w,v} \rangle+\langle \mathbf{w,w} \rangle$
$$=\lVert \mathbf{v} \rVert ^2+\mathbf{\lVert w \rVert }^2$$![[Cauchy-schwarz inequality]]