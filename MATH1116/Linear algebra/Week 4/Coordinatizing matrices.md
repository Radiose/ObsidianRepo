Firstly, note that $\mathcal{L}(\mathbb{F}^m,\mathbb{F}^n)$ and $Mat_{n \times m}(\mathbb{F})$ denote the same object. 

![[change of base matrix]]


# Theorem
If we have a [[linear map]] $T:V\to W$, with bases $\alpha,\beta$ of $V$ and $\gamma, \delta$ of $W$, then $$[T]_{\delta \leftarrow\beta}=X_{\delta \leftarrow\gamma }\circ[T]_{\gamma\leftarrow\alpha}\circ X^{-1}_{\beta \leftarrow\alpha}$$
![[Pasted image 20260823160629.png]]

This can be viewed on the above photo, but a formal proof will be supplied


The diagram above shows a couple things:
1: A matrix is a way of getting the scalars for one basis, and outputting the scalars for the vector after the linear transformation in the other basis. Thus, we represent each column in the matrix $[T]_{\gamma \leftarrow \alpha}$ as the basis vectors in $\alpha$ with each column as the coefficients of $\gamma$. So if $\alpha_{1}=c_{1}\gamma_{1}+\dots+c_{n}\gamma_{n}$, the column $1$ will be $(c_{1},\dots,c_{n})$
### Proof 




# Theorem 2
$U \xrightarrow[S]{}V \xrightarrow[T]{}W$
with bases $U = span(\beta),V=span(\alpha),W=span(\gamma)$

Then, $[TS]_{\gamma \leftarrow\beta}=[T]_{\gamma \leftarrow\alpha}[S]_{\alpha\leftarrow\beta}$

### Proof 




# Corollary 
Say $\alpha$, $\beta$ are bases of $V$ which is [[finite dimensional]].
If $T \in \mathcal{L}(V)$ is a [[linear operator]], then the [[trace]], $tr([T]_{\alpha})$ = $tr([T]_{\beta})$ and [[The determinant|determinant]] $\det([T]_{\alpha}) = \det([T]_{\beta})$.

### Proof 
This proof is accomplished using [[change of base matrix]] 
$$[T]_{\beta \leftarrow\beta}=X_{\beta \leftarrow\alpha}[T]_{\alpha \leftarrow\alpha}X_{\alpha \leftarrow\beta}$$ (via the theorem above) 
$\implies tr([T]_{\beta})=tr(X_{\beta \leftarrow\alpha}[T]_{\alpha \leftarrow\alpha}X_{\alpha \leftarrow\beta})$ 
$\implies tr([T]_{\beta})=tr(1 \cdot [T]_{\alpha \leftarrow\alpha})$ via the cyclic property of traces 
$\implies tr([T]_{\beta})=tr({[T]_{\alpha}})$
A very similar proof applies to the determinant proofs.
$\blacksquare$