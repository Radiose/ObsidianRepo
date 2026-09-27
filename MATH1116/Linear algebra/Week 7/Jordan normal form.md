If $V = \bigoplus_{t=1}^m G(\lambda_{i},T)$, then there exists a [[basis]] $\beta$ such that $\left[ T \right]_{\beta}$ = 

![[Pasted image 20260830160233.png|496]]

Except, instead of 0s, there are repetitions of eigenvalues.


# Theorem 
If $\mathbb{F}$ is [[algebraically closed field|algebraically closed]], and $\lambda_{1},\dots,\lambda_m$ are all distinct [[eigenvalue]]s of $T$, then  
$1:V= \bigoplus G(\lambda,T)$ 
2: $\exists$ a [[Jordan normal form]] for $T$

### Proof 
The key to this proof is to prove that if $\mathbb{F}$ is algebraically closed, then $T$ has an [[eigenvalue]].
#### Sub proof 
pick and $\mathbf{v}\in V \setminus \{ 0 \}$. Consider $\{ \mathbf{v},T(\mathbf{v}),\dots,T^n(\mathbf{v}) \}$, where $n:=\dim(V)$.
$\{ \mathbf{v},T(\mathbf{v}),\dots,T^n\mathbf{v} \}$ is [[Linearly dependent]] in $V$ via [[the basis theorem]] (too big).


Define $f(x):=a_{0}+a_{1}x+\dots+a_{n}(x)\in \mathbb{F}[x]$ so $\mathbf{0}=f()$