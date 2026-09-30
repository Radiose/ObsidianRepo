# Intuitive understanding of the algorithm 

This algorithm revolves around finding chains of eigenvectors. 
We first construct nested spaces $\ker N \subset \ker N^2 \subset\dots$
We record what new vectors occur at each level. 

$B_{r}$ corresponds to chains of length $r$, what our algorithm is attempting to do is to identify which newly added vectors should become the top of Jordan chains. 

After extracting the longest chains, we descend down. This is to basically ensure that each lower power kernel will have the eigenvector removed. For example, if $N^4(v)=0$, then we dont count that chain in the dimension of $\ker(N^3)$.

$C_{r}$ then aims to find the new chains of length $r$ after accounting for the longer chains we've already constructed. 

We continue until we reach the chains of length $1$.




### Algorithm for finding [[Jordan normal form]]

First, compute the characteristic polynomial $\chi_{T}(z)=\det(zI-T)$
Its roots are exactly $T$'s [[eigenvalue]]s, to the power of their algebraic multiplicities $d_{1},\dots,d_{k}$

For each $j=1,\dots,k$, do the following:
	- Set $N=T-\lambda_{j}I$, and find a basis of $\ker(N)$.
	- If $\dim(\ker(N))=d_{j}$, add the basis of $\ker(N)$ to the [[Jordan normal form|Jordan basis]] you are currently constructing, and go to the next $j$.

Otherwise, there are [[Jordan normal form|Jordan block]]s of size bigger than $1$. 
To find a Jordan basis in this case, we adapt the proof of ... 
1:
	 extend the basis $B_{1}:=\{ \mathbf{u}_{1},\dots,\mathbf{u}_{k} \}$ that you have already found of $\ker(N)$ to a basis of $\ker(N^2)$ by adding elements $B_{2}:=\mathbf{u}_{k+1},\dots,\mathbf{u}_{k_{2}}$, then extend to a basis of $\ker(N^3)$ by adding $B_{3}:=\mathbf{u}_{k_{2}+1},\dots,\mathbf{u}_{k_{3}}$ and so on, stopping when $k_{m}=d_{m}$ for the smallest $m>0$. Then, $m>0$ is the smallest integer such that $G(\lambda,T)=\ker(N^m)$
	
2:
	For $k_{m-1}< \ell\leq k_{m}=d_{m}$, add elements $\{ N^{m-1}\mathbf{u}_{\ell}\dots N\mathbf{u}_{\ell},\mathbf{u}_{\ell} \}$ to the [[Jordan normal form|Jordan basis]]. For a fixed $\ell,$ the [[span]] of these vectors will define a $T$ [[invariant subspace]], and in the basis of the subspace, $T$ can be represented by this $m\times m$ block, where empty spaces correspond to zeroes. 

![[Pasted image 20260930161040.png]]

3:
	Continue by descending induction on $r$, for $1\leq r<m$
	Observe that $N(B_{r+1})\cup N^2(B_{r+2})\cup\dots\cup N^{m-r}(B_{m})\subset \ker(N^r)\setminus \ker(N^{r-1})$.
	Find a subset $C_{r}\subset B_{r}$ such that $C_{r}\cup N(B_{r+1})\cup N^2(B_{r+2})\cup\dots\cup N^{m-r}(B_{m})$ is [[linearly independent]], and extends $B_{1}\cup \dots\cup B_{r-1}$ to a basis of $\ker(N^r)$.
	For each $\mathbf{u}_{\ell}\in C_r$, add elements $\{N^{r-1}\mathbf{u}_{\ell},\dots,N\mathbf{u}_{\ell},\mathbf{u}_{\ell} \}$ to the [[Jordan normal form|Jordan basis]]. Each of those sets will correspond to the $r\times r$ Jordan block $J_{\lambda_{j},r}$, appearing in the JNF of $T$.
	