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



# Theorem 2
Given $X,Y \subset V$, where $X$ is [[linearly independent]], and $Y$ spans $V$, then $|X|\leq|Y|$ (set [[cardinality]])
# Proof
Let 
$X = \{ v_{1},\dots v_{m} \}$
$Y=\{ w_{1},w_{2},\dots w_{m} \}$
Goal: Show $m \leq n$

Step 1:
Consider ${v_1} \cup Y$. It is linearly dependent, since $Y$ spans $V$ and thus $v_1 \in \text{span}(Y)$.

By the [[linear dependence lemma]], there exists $u \in {v_1} \cup Y$ such that $u \in \text{span}$ of the elements preceding it in the list, and removing $u$ doesn't change the span.

Since $v_1$ is first in the list, if $u = v_1$ then $v_1 = \vec{0}$ — but $v_1 \ne \vec{0}$ since $v_1 \in X$, a linearly independent set. So $u \ne v_1$, meaning $u = w_j \in Y$.

Set $Y_1 = Y \setminus {w_j}$. Then

$$V = \text{span}({v_1} \cup Y) = \text{span}({v_1} \cup Y_1)$$

with $|Y_1| = n - 1$.

Inductive step:
Consider $\{ v_{1}\dots v_{j} \}\cup Y_{j-1}$, it is linearly dependent. 
Via the [[linear dependence lemma]], $\exists w_{k}\in Y_{j-1}$. 
Call $Y_{j}:=Y_{j-1}\backslash\{ w_{k} \}$, then $V=span(\{ v_{1},v_{2},\dots,v_{j} \}\cup Y_{j})$
After step M:$|Y_{m}|=n-m\geq {0}$
So, $n \geq m \blacksquare$

The idea with the above proof is that linear independence is a stronger condition than span, and thus the minimal spanning set is the greatest set that is still [[linearly independent]]. 