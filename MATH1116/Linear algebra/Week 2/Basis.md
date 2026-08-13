A basis of a [[vector space]] is a [[linearly independent]], [[span|spanning]] set of [[vector]]s.

# Theorem 1
A set $X \subset V$ is a basis$\iff$ every vector $v \in V$ admits a **unique** expression as a [[Linear combination of vectors|linear combination]] of vectors from $X$.
$\implies$
Because $X$ is a basis, $\forall u \in V\quad \exists$ some linear comb such that 
$\mathbf{u}=a_{1}u_{1}+\dots+a_{n}v_{n}$ with $a_{i}\in \mathbb{F}$ and $\mathbf{u_{i}}\in X$
Suppose we had $v=a_{1}\mathbf{u}_{1}+\dots+a_{n}\mathbf{u}_{n}=\beta_{1}\mathbf{u}_{1}+\dots+\beta_{n}\mathbf{u}_{n}$
then $\mathbf{0}=\mathbf{v}-\mathbf{v}=(a-\beta)\mathbf{u_{1}}+\dots+(a_{n}-\beta_{n})\mathbf{u_{n}}$ 
Because every vector admits a unique expression, $a_{i}=\beta_{i}$ because $\mathbf{0}=0v_{1}+0v_{2}+\dots+ v_{n}$.

The other direction is easy. 

# Theorem 2 (linear independent list extends to a basis)
Every linearly independent set extends to a basis. 
### Proof
(this applies to finite lists). $X$ is finite (The linearly independent set). $V$ is [[finite dimensional]]. 
$X=\{ v_{1}\dots v_{m} \}$
$Y=\{ w_{1},\dots,w_{m} \}$ - a finite spanning set of $V$. 
$X\cup Y=\{ v_{1},\dots,v_{m},w_{1},\dots,w_{m} \}$

If $X\cup Y$ is linearly independent, then done. 
Otherwise, we apply the [[linear dependence lemma]] repetitively until we reach a linearly independent set $Z \subset X \cup Y$. By the lemma, $Span(Z)=Span(X \cup Y)=V$. Thus, $Z$ is a basis. 
Since $X$ is at the beginning of the list $X \cup Y$, with each application of the lemma, we remove some element of $Y$ and get $X \subset Z$ as required $\blacksquare$.

# Theorem 3
any $U \subset V$ has a complement, that is $\exists W\subset V s.t \quad V=U \oplus W$.
### Proof
pick some basis $X$ of $U$, we then extend it to some $X\cup Y$(via theorem 2) basis of $V$, where $Y$ are the remaining vectors from some spanning set of $V$.
Then, let $W=span(Y) = \{ w_{1},\dots,w_{j} \}$.

We aim to show $V=U\oplus W$. By [[internal direct sum of subspaces#Theorem 1|this theorem]], we aim to show that $V =U+W$, and $U \cap W=\{ \mathbf{0} \}$
Suppose $v \in V$, then $v$ can be written as a [[Linear combination of vectors|linear combination]] of the basis vectors $v =a_{1}u_{1}+\dots+a_{m}u+b_{1}w_{1}+\dots+b_{n}w_{n}$. Then, $v=\mathbf{u}+\mathbf{w}$ for some $\mathbf{u}\in U\quad\mathbf{v}\in V$. 
Thus, $V=U+W$.

To show $U \cap W = \{\mathbf{0}\}$, suppose $\mathbf{v} \in U \cap W$. Then there exist scalars $a_1, \dots, a_m, b_1, \dots, b_n \in \mathbb{F}$ such that

$$\mathbf{v} = a_1\mathbf{u}_1 + \cdots + a_m\mathbf{u}_m = b_1\mathbf{w}_1 + \cdots + b_n\mathbf{w}_n.$$

Thus

$$a_1\mathbf{u}_1 + \cdots + a_m\mathbf{u}_m - b_1\mathbf{w}_1 - \cdots - b_n\mathbf{w}_n = \mathbf{0}.$$

By the independence, we have $a_1 = \cdots = a_m = b_1 = \cdots = b_n = 0$. Thus $\mathbf{v} = 0$, completing the proof that $U \cap W = \{\mathbf{0}\}$. $\blacksquare$

The idea: create some complement from the vectors necessary to span the entire vector space. 
Start with U, add Y to get to V, then the complement is Y. 



# Theorem 4
if $\{ v_{1},v_{2},\dots v_{n} \}$ is a basis of $V$, then $\forall i\not=j\quad\forall \lambda \in \mathbb{F}$, $\{ v_{1},\dots,v_{i-1},v_{i}+b\vec{v}_{j},v_{i+1}\dots v_{n} \}$ is a basis as well.
### Proof 
Because the set is a basis, let some arbitrary $\mathbf{w \in }V$ be written
$$\mathbf{w} = a_1\mathbf{v}_1 + \cdots + a_{i-1}\mathbf{v}_{i-1} + a_i(\mathbf{v}_i + b\mathbf{v}_j) + a_{i+1}\mathbf{v}_{i+1} + \cdots + a_n\mathbf{v}_n.$$

We rearrange the sum to get

$$\mathbf{w} = a_1\mathbf{v}_1 + \cdots + a_{i-1}\mathbf{v}_{i-1} + a_i\mathbf{v}_i + a_{i+1}\mathbf{v}_{i+1} + \cdots + a_{j-1}\mathbf{v}_{j-1} + c\mathbf{v}_j + a_{j+1}\mathbf{v}_{j+1} + \cdots + a_n\mathbf{v}_n,$$
where $c=a_{j}+a_{i}b$. This proves existence. Now, because the original $\{ v_{1},v_{2},\dots v_{n} \}$ was a basis, the tuple of numbers $(a_{1},\dots,a_{j-i},c,a_{j+1},\dots,a_{n})$ is uniquely determined. But then we can recover $a_{j}=c-a_{i}b$. We test for uniqueness.

To check that the choice of $(a_1, \dots, a_n)$ is unique, we assume that we have a potentially different choice of $(c_1, \dots, c_n)$ such that

$$\mathbf{w} = a_1\mathbf{v}_1 + \cdots + a_{i-1}\mathbf{v}_{i-1} + a_i(\mathbf{v}_i + b\mathbf{v}_j) + a_{i+1}\mathbf{v}_{i+1} + \cdots + a_n\mathbf{v}_n$$
$$= c_1\mathbf{v}_1 + \cdots + c_{i-1}\mathbf{v}_{i-1} + c_i(\mathbf{v}_i + b\mathbf{v}_j) + c_{i+1}\mathbf{v}_{i+1} + \cdots + c_n\mathbf{v}_n.$$

We can write

$$0 = \mathbf{w} - \mathbf{w} = (a_1\mathbf{v}_1 + \cdots + a_{j-1}\mathbf{v}_{j-1} + (a_j + a_ib)\mathbf{v}_j + a_{j+1}\mathbf{v}_{j+1} + \cdots + a_n\mathbf{v}_n)$$
$$- (c_1\mathbf{v}_1 + \cdots + c_{j-1}\mathbf{v}_{j-1} + (c_j + c_ib)\mathbf{v}_j + c_{j+1}\mathbf{v}_{j+1} + \cdots + c_n\mathbf{v}_n)$$
$$= (a_1 - c_1)\mathbf{v}_1 + \cdots + (a_i - c_i)\mathbf{v}_i + \cdots + (a_{j-1} - c_{j-1})\mathbf{v}_{j-1}$$
$$+ (a_j - c_j + a_ib - c_ib)\mathbf{v}_j + (a_{j+1} - c_{j+1})\mathbf{v}_{j+1} + \cdots + (a_n - c_n)\mathbf{v}_n.$$

Since $\{\mathbf{v}_1, \dots, \mathbf{v}_n\}$ is a basis, it is in particular linearly independent, by definition of basis; hence the only linear combination of vectors summing to $0$ should have all coefficients $0$, by definition of linear independence. Therefore, the above equality implies that $a_k - c_k = 0$ for every $1 \le k \le n$ except for $k = j$ and $a_j - c_j + a_ib - c_ib = 0$. 

We thus get that $a_k = c_k$ for all $k \ne j$, and hence $0 = a_j - c_j + (a_i - c_i)b = a_j - c_j$, implying that $a_j = c_j$. 
This proves that the tuples of coefficients $(a_1, \dots, a_n)$ and $(c_1, \dots, c_n)$ are equal, which means that every vector $\mathbf{w}$ admits only one decomposition as a linear combination of $\{\mathbf{v}_1, \dots, \mathbf{v}_{i-1}, \mathbf{v}_i + b\mathbf{v}_j, \mathbf{v}_{i+1}, \dots, \mathbf{v}_n\}$. $\blacksquare$
