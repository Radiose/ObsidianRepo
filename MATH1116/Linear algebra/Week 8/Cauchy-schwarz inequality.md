For any $\mathbf{u,v}\in V$, $\left| \langle \mathbf{u},\mathbf{v} \rangle \right|\leq \lVert \mathbf{u} \rVert\cdot \lVert \mathbf{v} \rVert$

### Proof 
if $\mathbf{v}=\mathbf{0}$, its trivially true. 

For nonzero $\mathbf{v}$
Define $\mathbf{w}=\mathbf{u}- \frac{\langle \mathbf{u,v} \rangle}{\lVert \mathbf{u} \rVert}\mathbf{v}$
Note that $\langle \mathbf{w,v} \rangle=\langle \mathbf{u} - \frac{\langle \mathbf{u,v} \rangle}{\lVert \mathbf{v} \rVert^2}\mathbf{v},\mathbf{u} \rangle\rangle=\langle \mathbf{u,v} \rangle- \frac{\langle \mathbf{u,v} \rangle}{\lVert \mathbf{v} \rVert^2}\langle \mathbf{v,v} \rangle=0$    (because $\langle \mathbf{v,v} \rangle=\lVert \mathbf{v} \rVert^2$)

$\lVert \mathbf{u} \rVert^2=\left\lVert  \mathbf{w} + \frac{\langle \mathbf{u,v} \rangle}{\lVert \mathbf{u} \rVert^2}\mathbf{v} \right\rVert^2 =\lVert \mathbf{w} \rVert^2 + \left\lVert  \frac{\langle \mathbf{u,v} \rangle}{\lVert \mathbf{u} \rVert^2}\mathbf{v}  \right\rVert^2 = \lVert \mathbf{w} \rVert^2 + \langle \frac{\langle \mathbf{u+v} \rangle}{\lVert \mathbf{v} \rVert^2}\mathbf{v} + \frac{\langle \mathbf{u+v} \rangle}{\lVert \mathbf{v}^2 \rVert}\mathbf{v} \rangle \geq \frac{\langle \mathbf{u,v} \rangle\langle \mathbf{u,v} \rangle}{\lVert \mathbf{v} \rVert^2 \lVert \mathbf{v} \rVert^2} \langle \mathbf{v,v} \rangle= \frac{\lvert \langle \mathbf{u,v} \rangle \rvert^2}{\lVert \mathbf{v} \rVert^2}$
So $\lVert \mathbf{u} \rVert\lVert \mathbf{v} \rVert\geq \lvert \langle \mathbf{u,v} \rangle \rvert$
Note that this is an equality $\iff \mathbf{w}=0\iff \mathbf{u}\text{ is a scalar multiple}\iff \{ \mathbf{u,v} \}$ is [[Linearly dependent]]. $\blacksquare$

