If $T \in\mathcal{L}(V,W)$, then the dual map of $T$ is the [[linear map]] $$T^V \in \mathcal{L}(W^V,V^V)$$ defined by $$T^V(\phi)=\phi \circ T$$where $$\phi:W\to \mathbb{F}\text{ (an element of the dual vector space)}$$
Note that this is a linear map from one [[dual vector space]] to another. 

# Theorem 1
If $dim(V)$, $dim(W)<\infty$, and we have $\alpha$ as a basis of $V$, with $\beta$ as a basis of $W$, then 
$\forall \ \text{linear maps} \in \mathcal{L}(V,W)$, we have $[T^V]_{\alpha^V\leftarrow \beta^V}$ = $[T]^T_{\beta \leftarrow\alpha}$ 

(any matrix presentation of $T^V$ is the transpose of of the matrix presentation of $T$).

Come back when the time comes 



# Theorem 2 
If $S,T \in \mathcal{L}(V,W)$ and $U,W,V$ are vector spaces, then 
i) $(S+T)^V =S^V + T^V \quad \forall S,T \in \mathcal{L}(V,W)$
ii) $(\lambda T)^V=\lambda (T^V)\quad \forall \lambda \in \mathbb{F}\quad T\in \mathcal{L}(V,W)$
iii) $T \in \mathcal{L}(U,V),\ S \in \mathcal{L}(V,W) \implies (ST)^V=S^VT^V$

### Proof 
i)
Because both sides are dual maps, they must have domain of $W^V$. 
Pick $\phi:W \to \mathbb{F}$
Evaluate LHS:
$(S+T)^V (\phi)=\phi(S+T)=\phi \circ S + \phi \circ T$ via the linearity of $\phi$
$=S^V(\phi)+T^V(\phi)=RHS$
ii) Basically the exact same method 

iii) Pick $\phi \in W^V$
LHS($\phi$)=$(ST)^V \phi$=$\phi \circ(S\circ T)$ ) ($ST$) is defined as [[composition of Functions|composition]]
$= (\phi \circ T)\circ S = T^V ( \phi)\circ S=S^VT^V(\phi)=RHS$




