---
aliases:
  - converges absolutely
---
A series $\sum x_{j}$ is said to converge absolutely if $\sum_{j=0}^\infty|x_{j}|$ converges. 

## Remark 
A series $\sum x_{j}$ converges if it converges absolutely.
### Proof
let $\epsilon>0$. Pick $N \in \mathbb{N}$ such that $\forall m>n>N$
$|\sum_{j=n}^m x_{j}|<\sum_{j=n}^m |x_{j}|<\epsilon$
thus the sequence of partial sums $\left( \sum_{j=0}^n x_{j} \right)_{n \in \mathbb{N}}$ converges, thus the series must converge. 
