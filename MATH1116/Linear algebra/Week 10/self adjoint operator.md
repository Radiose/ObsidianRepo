# Definition 
For a [[linear operator]] $T$ over a finite dimensional [[inner product space]] $V$, we say that $T$ is self adjoint if $T=T^*$ (its [[adjoint linear map]])
IE, $\forall \mathbf{u,w}\in V,\langle T\mathbf{v},\mathbf{w} \rangle=\langle \mathbf{v},T\mathbf{w} \rangle$

Ex: If we have $S,T\in \mathcal{L}(V)$ which are self adjoint, and $\lambda \in \mathbb{R}$, then $S+T$, and $\lambda T$ are also self adjoint. 

Example:  If $T=id_{V}$, then $iT$ is not self adjoint  
This is because $\langle \mathbf{v},iT\mathbf{w} \rangle=-i\langle \mathbf{v},T\mathbf{w} \rangle\not=i\langle T\mathbf{v},\mathbf{w} \rangle$

Example 2: 
If $S,T$ are self [[adjoint linear map]], then $ST$ is not always self adjoint. 
$\begin{bmatrix}1  &  0 \\  0  & 0\end{bmatrix},\begin{bmatrix}0  & 1  \\  1  & 0\end{bmatrix}$ are both adjoint, but the composition isnt.

# Theorem 
Every [[eigenvalue]] of a self adjoint operator $T$ is real 

### Proof 
take some eigenvalue $\lambda \in C^*$, and any [[eigenvector]] $\mathbf{v}\in V$ with the corresponding eigenvalue. 
$\lambda \lVert \mathbf{v} \rVert^2=\lambda \langle \mathbf{v},\mathbf{v} \rangle=\langle \lambda \mathbf{v} ,\mathbf{v}\rangle=\langle T\mathbf{v},\mathbf{v} \rangle$ via def of eigenvector 
$=\langle \mathbf{v},T\mathbf{v} \rangle$ (self adjoint)
$=\langle \mathbf{v},\lambda \mathbf{v} \rangle=\bar{\lambda}\langle \mathbf{v},\mathbf{v} \rangle=\bar{\lambda} \lVert \mathbf{v} \rVert^2$
$\implies \lambda=\bar{\lambda}$ which happens only when $\lambda \in \mathbb{R}\ \ \blacksquare$

# Theorem 2
Assuming $\mathbb{F}=\mathbb{C}$
if $\forall \mathbf{v}\in V,\ \langle T\mathbf{v},\mathbf{v} \rangle=0$, then $T=\mathbf{0}$
### Proof 
We aim to show that $\forall \mathbf{u},\mathbf{v}\in V$, $\langle T\mathbf{u},\mathbf{w} \rangle=0$

Note that $4(T\mathbf{u},\mathbf{w})= \langle T(u+w), u+w\rangle - \langle T(u-w), u-w\rangle + i\langle T(u+iw), u+iw\rangle - i\langle T(u-iw), u-iw\rangle = 0$
And all of these inner products must be $=0$, via the assumption.
Then, $\mathbf{u}=\mathbf{w}$, $\mathbf{w}=T\mathbf{v}$ gives us $\langle T\mathbf{v},T\mathbf{v} \rangle=0\implies T\mathbf{v}=\mathbf{0}\forall \mathbf{v}\in V$ Thus, $T=\mathbf{0}$

## Important 
This does not hold for $\mathbb{F}=\mathbb{R}$
Rotation by $90^\circ \implies \begin{bmatrix}0  & -1  \\  1 & 0 \end{bmatrix}$  gives $\langle T\mathbf{v},\mathbf{v} \rangle=0$ for nonzero $T$ 

# Theorem 3 
If $T$ is **self adjoint**, and $\forall \mathbf{v}\in V\ \ \langle T\mathbf{v},\mathbf{v} \rangle=0\implies T=0$ (holds for $\mathbb{F}=\mathbb{R}$)

### Proof 
If $\mathbb{F}=\mathbb{C}$, we reference [[self adjoint operator#Theorem 2|theorem 2]]
If $\mathbb{F}=\mathbb{R}$, we use $4\langle T\mathbf{u},\mathbf{w} \rangle=\langle T(\mathbf{u}+\mathbf{w}),\mathbf{u}+\mathbf{w} \rangle-\langle T(\mathbf{u}-\mathbf{w}),\mathbf{u}-\mathbf{w} \rangle$ 