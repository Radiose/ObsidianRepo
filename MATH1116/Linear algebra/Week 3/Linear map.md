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


# basis of domain theorem 
![[basis of domain theorem]]

# Theorem 2
Any linear map between [[finite dimensional]] [[vector space]]s has a [[matrix]] representation.

### Proof 
Let $T:V\to W$. Pick a basis $\alpha=\{ a_{1},\dots a_{n} \}$ of $V$
$\beta=\{ b_{1},\dots b_{n} \}$
$\implies [T]_{\beta\to \alpha}:= \begin{bmatrix}  \\ [T(a_{1})]_{\beta_{1}}\dots[T(a_{n})]_{\beta}  \\  \\  \end{bmatrix}$
Where $[T(a_{i})]_{\beta_{i}}$ is the column of coordinates of $T(a_{i})\in W$ with respect to the basis $\beta$. So the representation of a basis vector of $V$ after undergoing a LT using $W$ basis. 


![[composition of linear maps]]

![[linear operator]]


# Kernel Theorem 
![[kernel#Theorem]]



# Theorem 3
Suppose $V$ and $W$ are finite-dimensional vector spaces such that $\dim V > \dim W$. Then

(i) no linear map from $V$ to $W$ is injective;

(ii) no linear map from $W$ to $V$ is surjective.

**Proof**

(i) Let $T \in \mathcal{L}(V, W)$. Then

$$\dim \operatorname{Ker} T = \dim V - \dim \operatorname{Range} T \geq \dim V - \dim W > 0,$$

where the equality above comes from the [[Rank nullity theorem]]. The inequality above states that $\dim \operatorname{Ker} T > 0$. This means that $\operatorname{Ker} T$ contains vectors other than $\mathbf{0}$. Thus $T$ is not injective by Theorem 3.5.

(ii) Exercise. $\blacksquare$
