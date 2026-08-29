# Definition 
The dual [[vector space]] of V is denoted $V^V=\mathcal{L}(V,\mathbb{F})$, which denotes the set of all [[linear functional]]s.

# Corollary
If $V$ is [[finite dimensional]], then $V^V$ is as well, and $\dim(V)=\dim(V^V)$

### Proof 
$\dim(V^V)=\dim(V)\cdot \dim(\mathbb{F})=\dim(V) \cdot {1}$
via [[linear map#Corollary|this]]



# Remark 
Now, the question is why do we call this a "dual"?
The answer is that we can view any $\mathbf{v}\in V$ itself as a [[linear functional]] on $V^V$, where it maps 
$\phi \in V^V$ to $\phi(\mathbf{v})\in \mathbb{F}$

We can denote this functional $ev_{v}:V^V \to\mathbb{F}$
or $ev_{v}\in V^{VV}$

# Theorem 
$ev:V\to V^{VV}$ is a [[linear map]]
where $\mathbf{v} \mapsto ev_{\mathbf{v}}$

### Proof 
Claim: $ev_{\mathbf{w}+\mathbf{v}}=ev_{\mathbf{w}}+ev_{\mathbf{v}}$
choose $\phi \in V^{V}$
$ev_{\mathbf{v}+\mathbf{w}}=\phi(\mathbf{v}+\mathbf{w})$ by definition of $ev_{v}$
$=\phi(v)+\phi(w)$ via linearity of $\phi$
$=ev_{v}(\phi)+ev_{\mathbf{w}}(\phi)=RHS$


# Remark 2
$v \in V$ and $T:\mathbb{F}\to V$ where $1 \mapsto \mathbf{v}$ are the same datum.
(this is because $T(c)=c\cdot T(1)$, so we are completely defined by $T(1)$)

# Corollary 
If $\dim(V)<\infty$, then $ev: V\to V^{VV}$ is an [[isomorphism]].
### Proof 
Note first that $\dim(V^{VV})=\dim(V^V)=\dim(V)$
Then, if we prove $\dim(\ker(ev))=\{ \vec{0} \}$, then it must be an isomorphism via [[Rank nullity theorem]]

Take $v \in V  \setminus \{ \mathbf{0} \}$
Extend $\{ \mathbf{v} \}$ to a basis $\{ \mathbf{v}, \mathbf{u}_{2},\dots,\mathbf{u}_{n} \}$ of $V$
Then, take the dual basis of $V^V =\{ \phi_{1},\dots,\phi_{n} \}$
$ev_{v}(\phi_{1})=\phi_{1}(v_{1})=1$ via the definition of $ev$, and via the definition of [[Dual basis]] vectors. 
Thus, $ev_{\mathbf{v}}$ **is not the zero functional**, so $\ker(ev)=\{ \mathbf{0} \}$


# Dual basis
![[Dual basis]]