A [[subset]] $U \subset V$ is a [[vector]] subspace if $U$ is a [[vector space]] with respect to the same operations of $+$ and $\cdot$ as $V$.

$\{ \mathbf{0} \}$ is a [[vector subspace]] of any $V$

$V$ is itself a subspace of $V$

The vector subspace of all formal polynomials with degree less than or equal to $d$ -
$\mathbb{F}{{[x]}}=\{ f(x) \in \mathbb{F}[x] \ | \ deg(x)\leq d\} \subset \mathbb{F}{[x]}$ 

$\mathbb{R} \subset \mathbb{C}$ is an $\mathbb{R}$ [[vector subspace]], but not a $\mathbb{C}$ vector subspace. 
This is because we can define $\mathbb{C}$ to be a vector space over $\mathbb{R}$. We cannot however make $\mathbb{R}$ a vector subspace of $\mathbb{C}$ over $\mathbb{C}$.


# Theorem
(very useful)
A subset $u \in V$ is a [[vector subspace]] $\iff$ the following hold:

i) $\mathbf{0}\in U$
ii) $\mathbf{u,w} \in U \implies \mathbf{u}+\mathbf{w}\in U$
iii) $\lambda \in F$, $\mathbf{u}\in U \implies \lambda \mathbf{u} \in U$

proof: All three conditions are directly satisfied via the definition of vector subspace

To prove conversely, we want to make sure that the axioms of [[vector space]] hold. 

All of the axioms are satisfied quite trivially, but the inverse $\mathbf{u}$ is hard. Via [[vector space#Theorem 1|the theorem from last time]], we can see that $-u = -1 \times u$ gives us the inverse.

