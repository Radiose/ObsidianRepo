trace 
the trace of a square [[Matrix]] $A$ is defined as the sum of all diagonal entries of $A$, denoted $\mathrm{Tr}(A)$.

**Lemma 1.3** (Trace is cyclic). If $A$ and $B$ are square matrices of the same size, then

$$\operatorname{tr}(AB) = \operatorname{tr}(BA).$$

**Proof.** Suppose

$$
A = \begin{pmatrix} A_{1,1} & \cdots & A_{1,n} \\ \vdots & & \vdots \\ A_{n,1} & \cdots & A_{n,n} \end{pmatrix}, \qquad
B = \begin{pmatrix} B_{1,1} & \cdots & B_{1,n} \\ \vdots & & \vdots \\ B_{n,1} & \cdots & B_{n,n} \end{pmatrix}.
$$

The $j^{\text{th}}$ term on the diagonal of $AB$ equals

$$
\sum_{k=1}^n A_{j,k} B_{k,j}.
$$

Thus

$$
\begin{aligned}
\operatorname{Tr}(AB) &= \sum_{j=1}^n \sum_{k=1}^n A_{j,k} B_{k,j} \\
&= \sum_{k=1}^n \sum_{j=1}^n B_{k,j} A_{j,k} \\
&= \operatorname{Tr}(BA)
\end{aligned}
$$

$\blacksquare$ 
The trick here was to treat the sums as sort of a nested loop. Inversion will maintain the same addition and multiplication (via the [[algebraic and order axioms|algebraic axiom]]s).
