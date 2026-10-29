# Definition 
An operator $S \in \mathcal{L}(V)$ is **positive** if it is [[self adjoint operator|self adjoint]], and $\forall \mathbf{v}\in V$, $\langle S \mathbf{v},\mathbf{v} \rangle\geq0$

# Theorem  
For finite dimensional $V$, and $S \in \mathcal{L}(V)$, the following statements are equivalent 
$\text{i})\quad S$ is positive
$\text{ii})\ \  S$ is self adjoint and has non negative [[eigenvalue]]s
$\text{iii})$ There exists some [[orthonormal vectors|orthonormal basis]] of $V$ such that the matrix presentation of $S$ in this basis is [[diagonalisable operator|diagonalisable]] with non negative real numbers on the diagonal.
$\text{iv})$ There exists some $T \in \mathcal{L}(V)$ such that $S=T^*T$

### Proof 
####  i) $\implies$ ii)
$S$ is self adjoint by definition 
Suppose $\mathbf{v}$ is an [[eigenvector]] of $S$
$\implies \langle S \mathbf{v},\mathbf{v} \rangle=\langle \lambda \mathbf{v},\mathbf{v} \rangle=\lambda \langle \mathbf{v},\mathbf{v} \rangle\geq 0$ by [[inner product]] axioms and $\mathbf{v}\not=\mathbf{0}$
#### ii) $\implies$ iii)
Since $S$ is self adjoint, we invoke the [[real spectral theorem]]
Since the diagonal entries of the matrix are precisely the [[eigenvalue]]s of $S$, they must be non negative by assumption in **ii)**

#### iii) $\implies$ iv)
First note that non negative reals have unique square roots. 
Choose an ON basis $\alpha$ as in **iii)**. 
Define $A$ as the [[matrix]] with diagonal entries $\sqrt{ \lambda_{1} },...,\sqrt{ \lambda_{n} }$
Define $T$ to be the operator whose matrix in the fixed basis $\alpha$ is $A$, then $S=T^2$.
This implies that $T$ is [[self adjoint operator|self adjoint]] via the [[real spectral theorem]].
Therefore $S=T^*T$ and the conclusion is satisfied
#### iv) $\implies$ i)
If $S=T^*T$, then $S^*=(T^*T)^*=T^*T$ so self adjoint.
To prove positivity, observe that $$\langle S\mathbf{v},\mathbf{v} \rangle=\langle T^*T \mathbf{v},\mathbf{v} \rangle= \langle T \mathbf{v},T\mathbf{v} \rangle  \geq 0 $$
via axioms of IP $\blacksquare$

