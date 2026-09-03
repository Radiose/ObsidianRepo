[[uniform convergence and L1 norm convergence of sequence of functions|uniform convergence]] of a [[series]]

# Definition 
Let $b > a$. Let $(f_{n})_{n\in \mathbb{N}}\in (\mathbb{R}^{[a,b]})^\mathbb{N}$

We say that $\sum_{n=0}^\infty f_{n}$ converges uniformly, if $\left( \sum_{n=0}^N f_{n} \right)_{n\in \mathbb{N}}$ converges uniformly. 

# Theorem 
Let $b>a$. Let $(f_{n})_{n\in \mathbb{N}}\in (\mathbb{R}^{[a,b]})^\mathbb{N}$

Assume that $\sum_{n=0}^\infty ||f_{n}||_{\infty}$ converges, then $\sum_{n=0}^\infty f_{n}$ converges uniformly. 

### Proof 
We use the assumption of [[uniformly Cauchy]].
Let $N,M \in \mathbb{N}$, with $M > N$. 
$$||\sum_{k=N}^M f_{k}||_{\infty}\leq \ \ \ sup_{x \in[a,b]} \sum_{k=N}^M |f(x)_{k}|$$ via the triangle inequality. 
$$\leq sup_{x \in [a,b]}\sum_{k=N}^M ||f_{k}(x)||_{\infty} = \sum||f_{k}||_{\infty}$$
Since $\sum||f_{k}||$ converges, via [[Convergence of series#Theorem 2 (converging series bounds smaller one)|comparison theorem]], $|| \sum_{k=N}^Mf_{k}||_{\infty}$ does as well, thus [[uniformly Cauchy]] and thereby [[uniform convergence and L1 norm convergence of sequence of functions|uniformly convergent]] $\blacksquare$

Importantly, this property lets us determine whether series of functions will converge via determining whether series of real numbers will, given by the sup norm, will converge, which is much easier. 