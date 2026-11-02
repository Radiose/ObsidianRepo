# Definition 
Let $T:V\to W$ be a linear map between finite dimensional vector spaces. 
For $s_{1},\dots,s_{r}$, the [[singular values]] of $T$, there exists [[orthonormal vectors|orthonormal]] lists $\alpha = \{ e_{1},\dots,e_{r} \}\in V$ and 
$\beta = \{ e_{1}',\dots,e_r' \} \in W$ such that $\forall \mathbf{v}\in V,$ we have $T\mathbf{v}=s_{1}\langle \mathbf{v},\mathbf{e}_{1} \rangle \mathbf{e}_{1}'+\dots+s_{r} \langle \mathbf{v},\mathbf{e}_{r} \rangle \mathbf{e}_{r}'$

By extending $\alpha$ and $\beta$ to [[basis]] $\alpha'$ and $\beta'$ of $V$ and $W$, we get that the matrix presentation of $T$ in these bases is diagonal, with [[singular values]] on the diagonal. 
![[Pasted image 20261029165110.png]]
(above $\mathcal{E}$ is obviously $\alpha'$ and $\mathcal{E}'$ is obviously $\beta'$)

### Proof 
Via [[singular values#Lemma|the lemma]], $T^*T$ is positive, so we can extract singular values of $T$.
By the [[real spectral theorem]], there exists [[orthonormal vectors|orthonormal basis]] $\mathbf{e}_{1},\dots,\mathbf{e}_{n}$ of $V$ where $n=\dim(V)$ such that $T^*T\mathbf{e}_{k}=s^2_{k}\mathbf{e}_{k}$ with $s_{k}=0$ for some $k\in \{ r+1,\dots,n \}$.
We define vectors in $W$ for $1\leq k \leq r$: $$\mathbf{e}_{k}':= \frac{1}{s_{k}}T\mathbf{e}_{k}$$
Now we check that $\{ \mathbf{e}_{1}',\dots,\mathbf{e}_{r} \}$ is orthonormal.

$\langle \mathbf{e}_{j}',\mathbf{e}_{k}' \rangle= \langle \frac{T\mathbf{e}_{j}}{s_{j}}, \frac{T{e_{k}}}{s_{k}} \rangle$
$=\frac{1}{s_{k}s_{j}}\langle T\mathbf{e}_{j},T\mathbf{e}_{k} \rangle$