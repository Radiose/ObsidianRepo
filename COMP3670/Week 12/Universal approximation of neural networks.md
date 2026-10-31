# Theorem 
Let $f$ be a [[multivariate continuity|continuous function]] defined on the hypercube $[0,1]^d$ 
$\forall\epsilon>0$, there is a one hidden layer [[neural network]] such that $$\zeta(\mathbf{x})=\sum_{i=0}^{d_{1}}w_{i}^{(2)}\sigma\left( \sum_{j=0}^d w_{i,j}^{(1)}x_{j} \right)$$
with $x_{0}=1$ and sigmoid [[activation function|activation]], such that $\lvert f(\mathbf{x})-\zeta(\mathbf{x}) \rvert<\epsilon$ for all $\mathbf{x}\in[0,1]^d$
