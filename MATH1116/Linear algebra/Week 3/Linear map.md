# Definition
A linear map between two sets  $V,W$ is a [[function]] $T:V \to W$ with the following properties:
- preservation of addition
	- $\forall \mathbf{u},\mathbf{v}\in V\quad T(\mathbf{u}+\mathbf{v})=T(\mathbf{u})+T(\mathbf{v})$
- It preserves scalar multiplication 
	- $\forall \lambda \in \mathbb{F},\ \forall \mathbf{u}\in V\quad T(\lambda \mathbf{u})=\lambda T(\mathbf{u})$
These can be combined into 
	$T(\lambda \mathbf{u}+\mu \mathbf{v})=\lambda T(\mathbf{u})+\mu T(\mathbf{v})$

### Examples 
1: the $\mathbf{0}$ map is linear 
2: $\mathcal{C}^1(\mathbb{R})\to C^0(\mathbb{R})$
3: $T(\mathbf{x}):=\mathbf{x}+1$ is NOT linear 

# Lemma 
If $T:V \to W$ is some linear map, then $T(\mathbf{0})=\mathbf{0}$
### Proof 
$T(\mathbf{0})$ is defined as $T(\mathbf{0}-\mathbf{0})$
$\implies T(\mathbf{0})+ (-T(\mathbf{0}))$
$\implies T(\mathbf{0})+(-1T(\mathbf{0}))$
$\implies T(\mathbf{0})-T(\mathbf{0})=\mathbf{0}$


# The set of all linear maps 
We denote $\mathcal{L}(V,W)$ as the set of all linear maps between $V$ and $W$
# Theorem
$\mathcal{L}(V,W)$ is a [[vector space]] with the operations of addition and scalar multiplication as follows 
given $\lambda \in \mathbb{F}$, $\quad S,T \in \mathcal{L}(V,W)$
$(T+S)(\mathbf{v})=T(\mathbf{v})+S(\mathbf{v})$
$(\lambda T)(\mathbf{v}):=\lambda \cdot T(\mathbf{v})$

### Proof
Verification of 8 vector space axioms 


# [[basis]] of domain theorem 
Suppose $X=\{ \mathbf{v}_{1},\mathbf{v}_{2}\dots \mathbf{v_{n}} \}$ is a basis of a vector space $V$. Suppose $\mathbf{w}_{1},\mathbf{w}_{2}\dots \mathbf{w}_{m}\in W$.
Then there exists some unique linear map $T:V \to W$ such that $T(\mathbf{v}_{j})=\mathbf{w}_{j}$ for each $j=1,\dots,n$.
### Proof 
#### Existence:
Given $\mathbf{v}\in V$, it has a basis decomposition $\mathbf{v}=a_{1}\mathbf{x}_{1}+\dots+a_{n}\mathbf{x_{n}}$ for some $a_{i}\in \mathbb{F},x_{i}\in X$
Let $T(\mathbf{v}):=a \mathbf{w}_{x_{1}}+\dots+a_{n}\mathbf{w}_{x_{n}}$.
We verify [[linearity]]
Let $\mathbf{v}=a_{1}\mathbf{x}_{1}+\dots+a_{n}\mathbf{x_{n}},\mathbf{u}=b_{1}\mathbf{x}_{1}+\dots+b_{n}\mathbf{x_{n}}$
$$
\begin{aligned}
T(\mathbf{u}+\mathbf{v}) &= T\big((a_1+b_1)\mathbf{v}_1 + \cdots + (a_n+b_n)\mathbf{v}_n\big) \\
&= (a_1+b_1)\mathbf{w}_1 + \cdots + (a_n+b_n)\mathbf{w}_n \\
&= (a_1\mathbf{w}_1 + \cdots + a_n\mathbf{w}_n) + (b_1\mathbf{w}_1 + \cdots + b_n\mathbf{w}_n) \\
&= T(\mathbf{u}) + T(\mathbf{v}).
\end{aligned}
$$

Similarly, if $\lambda \in \mathbb{F}$ and $\mathbf{v} = b_1\mathbf{v}_1 + \cdots + b_n\mathbf{v}_n$, then

$$
\begin{aligned}
T(\lambda \mathbf{v}) &= T(\lambda b_1 \mathbf{v}_1 + \cdots + \lambda b_n \mathbf{v}_n) \\
&= \lambda b_1 \mathbf{w}_1 + \cdots + \lambda b_n \mathbf{w}_n \\
&= \lambda(b_1\mathbf{w}_1 + \cdots + b_n\mathbf{w}_n) \\
&= \lambda T(\mathbf{v}).
\end{aligned}
$$
#### Uniqueness
Suppose $T \in \mathcal{L}(V,W)$ and that $T(\mathbf{v}_j) = \mathbf{w}_j$ for $j = 1,\dots,n$. Let $c_1,\dots,c_n \in \mathbb{F}$. The linearity of $T$ implies that

$$
T(c_1\mathbf{v}_1 + \cdots + c_n\mathbf{v}_n) = c_1\mathbf{w}_1 + \cdots + c_n\mathbf{w}_n.
$$

Thus $T$ is uniquely determined on $\text{span}\{\mathbf{v}_1,\dots,\mathbf{v}_n\}$. Because $\{\mathbf{v}_1,\dots,\mathbf{v}_n\}$ is a basis, we know $\text{span}\{\mathbf{v}_1,\dots,\mathbf{v}_n\} = V$. Hence $T$ is uniquely determined on $V$. $\blacksquare$

This theorem above is very important. It allows us to define any linear map solely by the values it take on a basis. 

# Theorem 2
Any linear map between [[finite dimensional]] [[vector space]]s has a [[matrix]] representation.

### Proof 
Let $T:V\to W$. Pick a basis $\alpha=\{ a_{1},\dots a_{n} \}$ of $V$
$\beta=\{ b_{1},\dots b_{n} \}$
$\implies [T]_{\beta\to \alpha}:= \begin{bmatrix}  \\ [T(a_{1})]_{\beta_{1}}\dots[T(a_{n})]_{\beta}  \\  \\  \end{bmatrix}$
Where $[T(a_{i})]_{\beta_{i}}$ is the column of coordinates of $T(a_{i})\in W$ with respect to the basis $\beta$. So the representation of a basis vector of $V$ after undergoing a LT using $W$ basis. 


![[composition of linear maps]]

![[linear operator]]
