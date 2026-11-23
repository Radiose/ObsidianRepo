# Commutativity of series and motivation
Given some finite sum $S_{N}=\sum_{i=1}^{N} a_{i}$, any orderings of the sums components will be equal if the series converges. 
This is intuitive, as $a_{1}+a_{2}+a_{3}+\dots+a_{N}=a_{2}+a_{1}+a_{3}+\dots +a_{N}$ via commutativity of addition. 

However, with an infinite series, more specific proofs are needed. We demonstrate two theorems that give interesting results. 

# Theorem 1
Let $\pi:\mathbb{N}\to \mathbb{N}$ be a bijection and let $\sum_{J=0}^\infty x_{j}$ [[absolute convergence|converge absolutely]]. 
Then, $\sum_{j=0}^\infty x_{\pi_{j}}$ converges absolutely, and $\sum_{j=1}^{\infty}x_{j}=\sum_{j=1}^{\infty}x_{\pi_{j}}$ 

### Proof 
let $\sum_{j=1}^\infty x_{j}$ converge absolutely, and let $\pi:\mathbb{N} \to \mathbb{N}$ be a bijection. 
Then, $\forall \epsilon >0\quad \exists N_{\epsilon} \in \mathbb{N}\quad \forall n,m \geq N_{\epsilon},\quad \sum_{j=m}^n \lvert x_{j} \rvert<\epsilon$
Let $\epsilon>0$. Then, $\pi^{-1}(\{ 1,\dots,N_{\epsilon} \})=\{ a_{1},\dots,a_{N_{\epsilon}} \}$. Note that this is a confusing step. We are getting the regular indices $1,2,\dots,N_{\epsilon}$ and getting the natural numbers $a_{1},\dots,a_{N_{\epsilon}}$ such that $\pi(a_{1})=1$ etc. 

Define $M_{\epsilon}:= max_{1 \leq k \leq N_{\epsilon}}\ a_{k}$. We have that $\forall j >M_{\epsilon}, \quad \pi(j)>N_{\epsilon}$. This is because we have already mapped to everything less than $N_{\epsilon}$

Similarly, let $j>k>M_{\epsilon}$. Then, $\forall \ell=k, \dots,j$, we have that $N_{\epsilon}<\min_{k \leq n \leq j} \pi({n})\leq \pi(\ell)\leq \max_{k\leq n \le j}$
Then, $\sum_{\ell=k}^j \lvert x_{\pi(\ell)} \rvert \le \sum^j_{m=\min_{k\leq n \leq j}\pi(n)}\lvert x_{m} \rvert<\epsilon$
Thus, $\sum_{\ell=0}^j \lvert x_{\pi_{\ell}} \rvert$ converges. 
Now we show equality. 
Let $\epsilon>0$
Pick $n>max(N\epsilon,M_{\epsilon})$.
Then, $\left\lvert  \sum_{j=0}^n x_{j}-\sum_{j=0}^n x_{\pi_{j}}  \right\rvert$

# Theorem 2 
Let $\sum_{j=1}^{\infty}x_{j}$ converge and $\sum_{j=1}^\infty \lvert x_{j} \rvert$ diverge. Let $x \in \mathbb{R}$. Then, there exists some $\pi:\mathbb{N} \to \mathbb{N}$ such that $\sum_{j=1}^\infty x_{\pi_{j}}$ converges, and $\sum_{j=1}^{\infty}x_{\pi_{j}}=x$,



