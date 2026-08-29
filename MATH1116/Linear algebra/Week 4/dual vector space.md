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

### Proof 
Claim: $ev_{\mathbf{w}+\mathbf{v}}=ev_{\mathbf{w}}+ev_{\mathbf{v}}$
choose $\phi \in V^{V}$
$ev_{\mathbf{v}+\mathbf{w}}=\phi(\mathbf{v}+\mathbf{w})$ by definition of $ev$
$=\phi(v)+\phi(w)$ via linearity of $\phi$
$=ev_{v}(\phi)+ev_{\mathbf{w}}(\phi)=RHS$

# Dual basis
![[Dual basis]]