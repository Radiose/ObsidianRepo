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
Thus  $(f(x)_{n})_{n\in \mathbb{N}} \in \mathbb{R}^\mathbb{N}$ is [[Cauchy sequence|cauchy]] and thereby convergent.


We define $$f(x)=\lim_{ n \to \infty }f_{n}(x)\ \ \forall x \in[a,b]$$

Because it is uniformly Cauchy, choose some increasing $(N_{j})_{j\in \mathbb{N}}\in \mathbb{N}^\mathbb{N}$ such that 
$$\forall j \in \mathbb{N}\ \ ||f-f_{N_{j}}||_{\infty} <2^{-j}$$
Note that $\sum_{j=0}^\infty f_{N_{j+1}}(x)-f_{N_{j}}(x)$ will converge (via inf geometric sequence)


Therefore, for $x \in[a,b]$, $$|f(x)-f_{N_{j}}(x)|= \lim_{ J \to \infty } |\sum_{k=j}^{J}\left[ f_{N_{k+1}}(x)-f_{N_{k}}(x)\right]|$$ Above we are passing these into a **telescoping sum** $$\leq \sum_{k=j}^J ||f_{N_{k+1}}-f_{N_{k}}||_{\infty}\leq 2^{-j}$$The final term is derived by [[Geometric Sequence]] identity on $2^{-k}$.

This gives $||f-f_{N_{j}}||_{\infty}\leq 2^{-j}\quad\forall j\in \mathbb{N}$

So, for $\epsilon>0$, choose $j \in \mathbb{N}$ such that $2^{-j}<\epsilon$, and such that $\forall m>N_{j}\quad ||f_{m}-f_{N_{j}}||_{\infty}<\epsilon$. 
Then, $\forall n >N_{j},\ \ ||f_{n}-f||_{\infty}\leq||f_{n}-f_{N_{j}}||_{\infty}+||f_{N_{j}}-f||_{\infty}\leq 2\epsilon$
