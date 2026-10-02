Note that these definitions follow from defining $\mathbb{F}:=\mathbb{C}$. For this reason, we have defined our inner product as the one shown in [[inner product#Examples]]

An inner product space is a [[vector space]] defined with an [[inner product]].

## Proposition 
(1) $\langle \mathbf{0},\mathbf{u} \rangle=0, \quad (2)\ \ \langle \mathbf{0},\mathbf{u} \rangle=0$
(3) $\langle  \mathbf{u},\mathbf{v+w}\rangle=\langle \mathbf{u,v} \rangle+\langle \mathbf{u,w} \rangle$
(4) $\langle \mathbf{u} ,\lambda \mathbf{v}\rangle=\overline \lambda \langle \mathbf{u},\mathbf{v} \rangle$
(5) $\langle \_,\mathbf{u} \rangle$ is a linear functional $V \to \mathbb{F}$ $\mathbf{v}\mapsto \langle \mathbf{v} ,\mathbf{u}\rangle$

### Proof 
$(5)$ follows from the additivity and homogeneity [[inner product#Consequences]]
$1$ follows from $5$
$(2):\ \ \langle \mathbf{u} ,\mathbf{0}\rangle=\overline{\langle \mathbf{0},\mathbf{u} \rangle}=\mathbf{0}$ 
$(4) \langle \mathbf{u},\lambda \mathbf{w} \rangle= \overline{\langle \lambda \mathbf{w},\mathbf{u} \rangle}=\overline{\lambda \langle \mathbf{w,u} \rangle}=\overline{\lambda}\langle \mathbf{u,w} \rangle$
$(3)$ is similar to $(4)\blacksquare$

#### Remark 
$\langle \mathbf{u},\_ \rangle$ is not a [[linear functional]] when $\mathbf{u}\not=\mathbf{0}$ and $\mathbb{F}=\mathbb{C}$, but $\overline{\langle \mathbf{u},\_ \rangle}$ is.


