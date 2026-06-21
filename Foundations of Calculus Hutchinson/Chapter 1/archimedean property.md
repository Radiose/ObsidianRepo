The following property of the [[real number|reals]] is not surprising. It follows from the [[algebraic and order axioms]] alone. Informally: there are no real numbers beyond the natural numbers. 

Theorem: For every real number $x$ there is a natural number $n$ such that $x <n$, equivalently, the set $\mathbb{N}$ is not bounded above. 


Proof:
Suppose that the theorem was false. Then there exists a [[real number]] $x$ such that $\forall n \in \mathbb{N}$ $x < n$. This implies $\mathbb{N}$ is bounded by a [[Completeness axiom|least upper bound]] $b$ by the completeness axiom. In other words.
$\forall n \in \mathbb{N} \ \ n \le b$ 
$\iff \forall n \in \mathbb{N} \ \ n+1 \le b$ 
$\iff \forall n \in \mathbb{N} \ \ n \le b-1$ 
In other words, $b-1$ is also an upper bound of $\mathbb{N}$, which contradicts that b is a least upper bound $\square$



A [[Corrolary]] that follows from this, which is important to prove the [[Density of the rational and irrational numbers]].

For any [[real number]] $\epsilon> 0$, there is a natural number $n$ such that $\frac{1}{n}< \epsilon$.

Proof: by the Archimedean property: there is a natural number $n$ such that $n > \frac{1}{\epsilon}$. But then $\frac{1}{n} < \epsilon$.

