Suppose $V$ is a finite dimensional inner product space over $\mathbb{C}$ and that $T \in \mathcal{L}(V)$ is some operator on $V$. Then, $T$ is [[diagonalisable operator|diagonalisable]] with respect to an [[orthonormal vectors|orthonormal basis]], and the diagonal entries are real $\iff T$ is [[self adjoint operator|self adjoint]].

### Proof 
$\impliedby$
We run an induction argument similar to that done in the [[real spectral theorem]], with $n=\dim(V)$
for $n=1$, the argument is trivial 

For our inductive case, suppose $\dim(V)=n-1$, and that it is diagonalisable with respect to some orthonormal basis.
Because $\mathbb{C}$ is [[algebraically closed field|algebraically closed]], $T \in \mathcal{L}(V)$ must have some eigenvalue via [[algebraically closed field#Theorem 1|this theorem]].
We can then divide it by its norm to get a vector with length 1, denote it $\mathbf{u}$.
Let $U=span\{ \mathbf{u} \}$
Then, $U$ is a one dimensional subspace of $V$ that is invariant under $T$. Thus, $T_{U^\perp} \in \mathcal{L}(U^\perp)$ is [[self adjoint operator|self adjoint]] via [[self adjoint operator#Theorem 5|this theorem]], and of dim $n-1$
Then via the induction hypothesis, there is some orthonormal basis of $U^\perp$ consisting of eigenvectors of $T_{U^\perp}$. Adding $\mathbf{u}$ to this makes the basis 