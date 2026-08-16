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

