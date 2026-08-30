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
