This is another test that we are able to use to determine whether some [[series]] converges. It in particular determines whether very strong convergences occur, or whether very weak convergences occur. This will become apparent in the proof. 

# Theorem 
Let $(x_{j})_{j \in \mathbb{N}}\in \mathbb{R}^\mathbb{N}$. Assume that $\lim_{ j \to +\infty } \frac{x_{j+1}}{x_{j}}=\ell$. If $\ell \in[0,1)$, then $\sum_{j=0}^\infty$ converges. If $\ell \in(1,\infty)$, then $\sum_{j=0}^\infty x_{j}$ diverges. 

### Proof 
Case 1:
Pick $\epsilon =\frac{1-\ell}{2}$. Then, $\exists N\in \mathbb{N}$ such that $\forall j \geq N,\ |\frac{x_{j+1}}{x_{j}}-\ell|\leq \frac{1-l}{2}$. 
$\forall j \geq N$, $\frac{x_{j+1}}{x_{j}}\leq \ell + \frac{1-\ell}{2}=\frac{1+\ell}{2}$
Via [[Induction]], 
$\forall j\geq N\quad x_{n}\leq\left( \frac{1+\ell}{2} \right)^{j-N} x_N$
Let $y_{j}=\left( \frac{1+\ell}{2} \right)^{j-N}$
Because $\ell \in[0,1)$, $\sum _{j=0}^\infty y_{j}$ converges. 
Additionally, $x_{j}\leq y_{j} \forall j \in \mathbb{N}$
Thus, $\sum^\infty x_{j}$ converges, via [[Convergence of series#Theorem 2 (converging series bounds smaller one)|the comparison theorem]].
Case 2:
Pick $\epsilon=\frac{\ell-1}{2}$, then $\exists N\in \mathbb{N}$ $\forall n\geq N$  $|\frac{x_{j+1}}{x_{j}} -\ell| \leq \frac{\ell-1}{2}$

So for all $j \geq N$,

$$\frac{x_{j+1}}{x_j} \geq \ell - \left| \frac{x_{j+1}}{x_j} - \ell \right| \geq \ell - \frac{\ell - 1}{2} = \frac{\ell + 1}{2}.$$

For all $j \geq N$,

$$x_{j+1} \geq \left( \frac{\ell+1}{2} \right) x_j.$$

By induction,

$$x_j \geq \left( \frac{\ell+1}{2} \right)^{j-N} x_N, \quad \forall j \geq N.$$

Since $\frac{\ell+1}{2} > 1$, then

$$\sum_{j=N}^{\infty} \left( \frac{\ell+1}{2} \right)^{j-N} x_N$$

diverges, and so does $\sum_{j=0}^{\infty} x_j$.