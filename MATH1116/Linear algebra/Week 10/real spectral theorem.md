# Building up to it 

# Theorem 1
Let $T \in \mathcal{L}(V)$ and [[self adjoint operator|self adjoint]]
Suppose $b,c \in \mathbb{R}$ such that $b^2 < 4c$
Then, $T^2+bT+c$ is [[invertible linear map|invertible]]

### Proof 
Define $S$ by $T^2+bT+c$
We have a goal here, to show that $\forall \mathbf{v} \in V$ ,$\mathbf{v}\not=0 \implies \langle S\mathbf{v},\mathbf{v} \rangle\not=0$
If this is true, then $\ker(S)=\{ \mathbf{0} \}$

Let $\langle S\mathbf{v},\mathbf{v} \rangle=\langle T^2\mathbf{v} +bT\mathbf{v}+^{3}c \mathbf{v},\mathbf{v} \rangle$
$= \langle T^2 \mathbf{v} \rangle+b\langle T\mathbf{v},\mathbf{v} \rangle+ c\langle \mathbf{v},\mathbf{v} \rangle$
$=\langle T\mathbf{v},T\mathbf{v} \rangle+\langle T,\mathbf{v},\bar{b}\mathbf{v} \rangle+c \lVert \mathbf{v} \rVert^2$

$\geq \lVert T\mathbf{v} \rVert^2 +\lVert T\mathbf{v} \rVert+b \lVert \mathbf{v} \rVert+c \lVert \mathbf{v} \rVert^2$
$= \lVert \mathbf{v} \rVert^2 \left( \left( \frac{\lVert T\mathbf{v} \rVert}{\lVert \mathbf{v} \rVert} \right)^2+ b \frac{\lVert T\mathbf{v} \rVert}{\lVert \mathbf{v} \rVert}+c\right)>0$ 
Note that this appears as a quadratic equation 
So, we say that $>0$ by assumption that $b^2 <4ac$, thus $\not=0$ and invertible.

# Proving that $T$ has an [[eigenvalue]]

#### 1:
Choose any $\mathbf{v} \in V \setminus \{ \mathbf{0} \}$ and $n=\dim(V)$
$\implies \{ \mathbf{v} ,T\mathbf{v},T^2\mathbf{v},\dots,T ^n\mathbf{v}\}$ must be linearly dependent. 
Pick scalars $a_{0},\dots,a_{n}$ such that not all $=0$ and $a_{0}\mathbf{v}+a_{1}T\mathbf{v}+\dots+a_{n}T^n\mathbf{v}=0$
Choose $m$ as the maximal index such that $a_{m}\not=0$
#### 2:
Via the [[Fundamental theorem of algebra]], denote 
$f(z)=a_{m}(z-\lambda_{1})\dots(z-\lambda_{m})$ with $\lambda_{i}\in \mathbb{C}$
If $\lambda_{i}\not\in \mathbb{R}$, then there must be a [[complex conjugate]]
$(z-\lambda_{i})(z-\bar{\lambda_{i}})=z^2-(\lambda_{i}+\bar{\lambda_{i}}z+\lambda_{i} \bar{\lambda_{i}})$
Thus we can conclude that 
$f(z)=a_{m}((z-\lambda_{i})\dots(z-\lambda_{k})(z^2+b_{1}z+c_{1})\dots(z^2+b_{i}z+c_{i})$
Note that $m=k+2l$
If $k=0$, then we will have no eigenvalues via this logic 
Note that $z^2+b_{i}z+c_{i}$ is a quadratic with no real solutions, thus its discriminant is less than $0$, thus $b^2<4c$.

#### 3
If $T$ is self adjoint, then by the [[real spectral theorem#Theorem 1|theorem 1]], each of of $T^2 +b_{i}T+c_{j}id$ is invertible, 
But by $1$, $f(T)(\mathbf{v})=0$ so not invertible 
Thus, some $(T-\lambda_{i})\mathbf{v}=\mathbf{0}$ so $T$ has some eigenvalue. 

## Conclusion 
If $T$ is self adjoint, it has an eigenvalue. 

# The real spectral theorem 
Suppose $V$ is a non trivial [[inner product space]] over $\mathbb{R}$. Then, T is [[diagonalisable operator|diagonalisable]] with respect to an [[orthonormal vectors|orthonormal basis]] $\iff$ $T \in \mathcal{L}(V)$ is [[self adjoint operator|self adjoint]]
