---
aliases:
  - spanned
---
Span
Given a set of $p$ vectors $v_{1},v_{2},\dots v_{p}$, the set of all possible linear combinations of these vectors is the span.
We denote it as span{$v_{1},v_{2}\dots v_{p}$}.

We note that the Span$(X)$ is a [[vector subspace|subspace]].

Some examples:
Span$\{ \emptyset \}=\mathbf{0}$
Span$\{ V \}=V$

# Theorem 1
Given a [[subset]] $X$, its span is the smallest [[vector subspace|subspace]] of $V$ that contains $X$.
# Proof
Suppose that $U$ is a subspace of $V$ s.t $U \subset Span(X)$ and $X \subset U$
Take some element of $\lambda_{1} v_{1}+\dots+\lambda_{m}v_{m} \in Span(X)$
$v_{1},\dots v_{n}\in X \in U$, but $U$ is a subspace, so $\lambda_{1} v_{1}+\lambda_{2}v_{2}+\dots+\lambda_{n}v_{n} \in U$ (subspaces have addition and multiplication closed).
thus, $Span(X)=U$
