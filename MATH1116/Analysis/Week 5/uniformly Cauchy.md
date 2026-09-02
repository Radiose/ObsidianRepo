let $b>a$, $f_{n}:[a,b)\to \mathbb{R}$ $f : [a,b]\to \mathbb{R}\ \ \forall n\in \mathbb{N}$
The [[sequence]] $(f_{n})_{n \in \mathbb{N}}$ is said to be [[uniformly Cauchy]] if 
$$\forall\epsilon>0\ \ \exists N\in \mathbb{N}\ \ \forall n>m\geq N \implies ||f_{n}-f_{m}||_{\infty}<\epsilon$$
# Theorem 
if $(f_{n})_{n\in \mathbb{N}}\in(\mathbb{R}^{[a,b]})^\mathbb{N}$ is [[uniformly Cauchy]], then it is uniformly convergent. 

### Proof 
let $\epsilon>0$. Let $x \in[a,b]$
Assume $$\forall\epsilon >0\ \ \exists N\in \mathbb{N} \ \ \forall n,n>N \implies||f_{n}-f_{m}||_{\infty} <\epsilon$$
Let $x \in[a,b]$
$$\forall\epsilon>0 \ \ \  \exists N \in \mathbb{N}\ \ \ \forall n,m \geq N \implies|f_{n}(x)-f_{m}(x)|<\epsilon$$
Then $(f_{n})_{n\in \mathbb{N}} \in \mathbb{R}^\mathbb{N}$ is [[Cauchy sequence|cauchy]] and thereby convergent.
We define $f(x)=\lim_{ n \to \infty }f_{n}(x)$ $\forall x \in[a,b]$
By uniformly Cauchy, choose $(N_{j})_{j\in \mathbb{N}}\in \mathbb{N}^\mathbb{N}$ such that 
$$\forall j \in \mathbb{N}\ \ ||f_{N_{j+1}}-f_{N_{j}}||_{\infty} <2^{-j}$$
Therefore, for z