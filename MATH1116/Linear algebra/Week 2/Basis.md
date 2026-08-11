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
pick some basis $X$ of $U$, we then extend it to some $X\cup Y$, where $Y$ is some spanning set of $V$.
Then, $W=span(Y)$.
