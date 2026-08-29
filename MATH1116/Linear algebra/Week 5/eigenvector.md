# Definition 
an eigenvector with eigenvalue $\lambda$ is a non-zero vector $v \in V \setminus \{ \mathbf{0} \}$ such that $T \mathbf{v}=\lambda \mathbf{v}$


# Theorem 
Let $T \in \mathcal{L}(V)$
Suppose $\{ \mathbf{v_{1}},\dots,\mathbf{v_{n}} \}\in V$ are [[eigenvector]]s of $T$
Then, $\{ \mathbf{v_{1}},..,\mathbf{v_{n}} \}$ is [[linearly independent]]
### Proof 
Via contradiction, assume that $\{ \mathbf{v_{1}},\dots,\mathbf{v_{n}} \}$ is [[Linearly dependent]]
Then, via [[linear dependence lemma]], $\exists j \ s.t$ $\mathbf{v}_{j}\in span \{ \mathbf{v}_{1},\dots,\mathbf{v}_{j-1} \}$
Note that $j \not=1$ because [[eigenvector]]s cannot $= \mathbf{0}$
