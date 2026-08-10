Suppose $X=\{ v_{1},\dots v_{m} \}$ is a [[Linearly dependent]] set.
Then, $\exists j\in\{1,\dots m \}$ such that:
1:$v_{j}\in Span(v_{1},\dots,v_{j-1})$
2: $Span\{ v_{1},\dots v_{m} \}=Span\{ v_{1},v_{2}\dots \hat{v_{j}},\dots,v_{m} \}$
Proof:
Case $v_{1}=\vec{0}$. Then, pick $j=1$.
Trivially, $span\{{\emptyset}\}=\mathbf{0}$
Additionally, because $span\{ \mathbf{0} \}=\mathbf{0}$,$span\{ v_{1},v_{2},\dots,\hat{v_{j}},\dots v_{m} \}=span\{ v_{1},\dots,v_{n} \}$
Case $v_{1}\not=0$
The goal here is to show $m \leq n$

Choose the smallest $j > 1$ such that $\{\mathbf{v}_1, \ldots, \mathbf{v}_j\}$ is linearly dependent. 
By definition of linear dependence, there exist constants $a_1, \ldots, a_j \in \mathbb{F}$ such that $a_1\mathbf{v}_1 + \cdots + a_j\mathbf{v}_j = \mathbf{0}$, but not all of the constants are zero. 
I claim that $a_j \neq 0$. Indeed, if it happened that $a_j = 0$, then we would get a smaller non-trivial linear combination $a_1\mathbf{v}_1 + \cdots + a_{j-1}\mathbf{v}_{j-1} = \mathbf{0}$ that sums to zero; but this contradicts the minimality of the chosen $j$. Now that we know that $a_j \neq 0$, we can use axiom (F10) of fields to find the inverse of $a_j$ and get the following equation:

$$
\mathbf{v}_j = -(a_j)^{-1}a_1\mathbf{v}_1 - \cdots - (a_j)^{-1}a_{j-1}\mathbf{v}_{j-1}.
$$

This shows that $\mathbf{v}_j \in \text{Span}\{\mathbf{v}_1, \ldots, \mathbf{v}_{j-1}\}$.
The first bullet point should now imply the second. 
