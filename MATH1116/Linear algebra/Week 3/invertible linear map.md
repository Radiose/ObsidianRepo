---
aliases:
  - invertible
  - inverse
---
A [[linear map]] $T: V\to W$ is invertible if there exists a [[linear map]] $S:W \to V$ such that $S \circ T=id_{V}$ and $T \circ S=id_{W}$. Such a map is called the inverse of $T$ and is denoted by $T^{-1}$

# Theorem 
An invertible [[linear map]] has a unique inverse. 

Proof:
Suppose $T \in \mathcal{L}(V,W)$ is invertible, and $S_{1},S_{2}$ are inverses. 
Then, $S_{1}=S_{1}I=S_{1}(TS_{2})=(S_{1}T)S_{2}=IS_{2}=S_{2}$

# Theorem
A [[linear map]] $T:V \to W$ is invertible if and only if it is a [[Bijective Transformation]]


