the [[relative entropy]] between two distributions $p(x)$ and $q(x)$ with $X \in \mathcal{X}$ is non negative. 
$$D_{kl}(p ||q)\geq 0$$
with equality if and only if $p(x)=g(x) \forall x$ 

# Proof 
Recall that:

$$D_{KL}(p\|q)=\sum_{x\in\mathcal{X}}p(x)\log\frac{p(x)}{q(x)}
=\mathbb{E}_{p(X)}\left[\log\frac{p(X)}{q(X)}\right]$$

Let $\mathcal{A}=\{x:p(x)>0\}$. Then:

$$-D_{KL}(p\|q)
=\sum_{x\in\mathcal{A}}p(x)\log\frac{q(x)}{p(x)}$$

$\leq\log\sum_{x\in\mathcal{A}}p(x)\frac{q(x)}{p(x)}$

$\quad$ ([[Jensens Inequality]])

$=\log\sum_{x\in\mathcal{A}}q(x)$

$\leq\log\sum_{x\in\mathcal{X}}q(x)$

$=\log 1$

$=0$