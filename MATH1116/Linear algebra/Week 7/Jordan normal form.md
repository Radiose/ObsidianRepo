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
Then $\exists a_{0},a_{1},\dots,a_{n}$ such that $(a_{0}\cdot id+\dots+a_{n}T^n)(\mathbf{v})=\mathbf{0}$

Define $f(x):=a_{0}+a_{1}x+\dots+a_{n}(x)\in \mathbb{F}[x]$ so $\mathbf{0}=f(T)(\mathbf{v})$
$\implies f(T)$ is not invertible 
Call $d:=deg(f(x))$, then $f(x)=a_{d}(x-r_{1})(x-r_{2})\dots(x-r_{d})$ via the [[Fundamental theorem of algebra]]

Then, $f(T)=a_{d}(T-r \cdot id)\dots(T-r\cdot id)$
$\implies \exists i$ such that $(T-r\cdot id)$ is not invertible $\implies \ker(T-r_{i}\cdot id)\not=\{ 0 \}$
$\implies r_{i}$ is an eigenvalue $\implies T$ has an eigenvalue $\blacksquare$


####  Rest of proof 
$U=\bigoplus G(\lambda_{i},T)$
We want $\mathbf{w} \in V$ such that $\mathbf{w}$ is [[invariant subspace|invariant]] under $T$, and that $W \oplus U=V$
If we find such a W, then if $W \not=\{ 0 \}$, then $T|_{w}$ has an eigenvalue, contradicting the original statement.
Define $g(x):=(x-\lambda_{1})\dots(x-\lambda_{m})$
Define $S :=G(T)$
##### Observe 
$(1)\ \ U = \ker(S^n)$
Because $RHS=\ker((T-\lambda_{1}\cdot id)^n\dots(T-\lambda_{m}\cdot id)^n)=\ker(T-\lambda_{1}id)^n+\dots+\ker(T-\lambda_{n}\cdot id)^n$
$=G(\lambda,T)\oplus\dots \oplus G(\lambda_{m},T)=U$

$(2)$ Define $W=Range(S^n)$, then $U \cap W=\{ 0 \}$
Take $\mathbf{v}\in U \cap W$,  then, $\exists \mathbf{w}\in V$ such that $S^n(\mathbf{w})=\mathbf{v}$
Note that $\ker(S^n)=\ker(S^{2n})$, and $S^{2n} \mathbf{w }=\mathbf{0}\implies S^n(\mathbf{w})=\mathbf{0}$

$(3)$ so $U \oplus W \subseteq V$, and by [[Rank nullity theorem]], $\ker(s^n)\oplus Range(S^n)=V$

