# Definition 
For $W,V$ being linear, finite dimensional inner product spaces

The adjoint of a linear map, $T:V\to W$ is a [[linear map|map]] $T^*:W\to V$ such that
$$\forall \mathbf{v}\in V\quad\forall\mathbf{w}\in W\ \ \langle T\mathbf{v},\mathbf{w} \rangle=\langle \mathbf{v},T^*\mathbf{w} \rangle$$
Exercise:
If $T^*$ exists, it is a linear ma 

# Theorem 
If $V$ is finite dimensional, then $\forall \phi \in V^V$, $\exists! \mathbf{v}\in V$ such that $\forall \mathbf{u}\in V$, $\phi(\mathbf{u})=\langle \mathbf{u},\mathbf{v} \rangle$

### Proof 
We establish that $\Phi_{V}:V\to V^V$ is an [[isomorphism]], so $\exists!\mathbf{w}\in V$ such that $\Phi_{V}(\mathbf{w})=\psi$
Then, $\phi=\Phi(\mathbf{w})=\langle \_{},\iota(\mathbf{w}) \rangle$. Because $\iota$ is bijective, and $\Phi$ is isomorphic, $\phi$ is unique. 

