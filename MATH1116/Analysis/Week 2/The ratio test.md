This is another test that we are able to use to determine whether some [[series]] converges. It in particular determines whether very strong convergences occur, or whether very weak convergences occur. This will become apparent in the proof. 

# Theorem 
Let $(x_{j})_{j \in \mathbb{N}}\in \mathbb{R}^\mathbb{N}$. Assume that $\lim_{ j \to +\infty } \frac{x_{j+1}}{x_{j}}=\ell$. If $\ell \in[0,1)$, then $\sum_{j=0}^\infty$ converges. If $\ell \in(1,\infty)$, then $\sum_{j=0}^\infty x_{j}$ diverges. 

### Proof 
Case 1:
Pick $\bar{\ell} =\frac{1-\ell}{2}$. Then, $\exists N\in \mathbb{N}$ such that $\forall j \geq N,\ |\frac{x_{j+1}}{x_{j}}-\ell|\leq \frac{1-l}{2}$. 
$\forall j \geq N$, $\frac{x_{j+1}}{x_{j}}\leq \ell + \frac{1-\ell}{2}=\frac{1+\ell}{2}$
