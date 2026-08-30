---
aliases:
  - diagonalisable
---
# Motivation 
If $V=E(\lambda_{1};T)\oplus\dots \oplus E(\lambda_{m};T)$, then we can study $T$ on each $E(\lambda_{i};T)$
Note that $T$ restricted to $E(\lambda_{i};T)$ is $\lambda_{i}\cdot id_{E(\lambda_{i};T)}$ 

# Definition 
a [[linear operator]] $T \in \mathcal{L}(V)$ is called *diagonalisable* if $V$ has a [[basis]] consisting of [[eigenvector]]s of $T$.
OR
A linear operator is [[diagonalisable operator|diagonalisable]] if $V=E(\lambda_{1};T)\oplus\dots \oplus E(\lambda_{m};T)$

# Example 
$D:\mathbb{R}[x]\to \mathbb{R}[x]$, $D(x^n)=nx^{n-1}$, $D(1)=0$
Note $\ker(D)=span\{ 1 \}$
Thus, $0$ is the unique [[eigenvalue]] ($T(\mathbf{v})=0 \times \mathbf{v}$ when $\mathbf{v}\in span\{ 1 \}$).
(uniqueness can be checked)
Thus, our eigenspace is $E(0;T)$, which has a the basis of $\{ 1 \}$, so its dimension is $1$.
But, $\dim(V)=\infty$, so $V$ cannot have a basis comprised from $span\{ 1 \}$
Thus $D$ is not [[diagonalisable operator|diagonalisable]].


# Theorem 
If $V$ is [[finite dimensional]], and $T$ has $\dim(V)$ distinct [[eigenvalue]]s, then $T$ is [[diagonalisable operator|diagonalisable]].

### Proof 
Let $n:=\dim(V)$, let $\lambda_{1},\dots,\lambda_{n}$ be distinct [[eigenvalue]]s.
Via [[eigenvector#Theorem 1|this theorem]], $\{ \mathbf{v}_{1},\dots,\mathbf{v_{n}} \}$ are linearly independent. 
Thus, it must be a [[basis]].

### Remark: this is sufficient, but not necessary.
There can be [[diagonalisable operator|diagonalisable]] matrices that have less than $\dim(V)$ eigenvalues 
Example 
$\begin{bmatrix}5,0,0 \\  0,5,0 \\  0,0,5\end{bmatrix}$ - obviously diagonalisable but at the same time one one distinct eigenvalue 

