---
aliases:
  - first principle component
---
A first principle component is a unit vector $\mathbf{q}$ maximising  $\mathbf{q}^T\mathbf{Cq}$.
The numbers $\langle \mathbf{q},\mathbf{x_{i}} \rangle$ are the corresponding principle component scores of the datapoints. 


# Theorem 
Let $\mathbf{C}$ have some [[orthonormal vectors|orthonormal]] eigenbasis $\mathbf{q_{1}},\dots,\mathbf{q}_{n}$, ordered in which the eigenvalues satisfy         $\lambda_{1}\geq\dots\geq \lambda_{n}\geq{0}$
Then, $\max_{\lVert q \rVert_{2}=1}\mathbf{q}^T \mathbf{C}\mathbf{q}=\lambda_{1}$
The unit vectors in the eigenspace of $\lambda_{1}$ are the maximisers. In particular, $\mathbf{q}_{1}$ is a first principle component direction.



![[Principle component analysis]]