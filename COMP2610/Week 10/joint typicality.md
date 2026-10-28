Recall the definition of the typical set 
![[typical set#Definition]]


# Definition 
A pair of [[sequence]]s $\mathbf{x}\in \mathcal{A}_{X}^N$, and $\mathbf{y}\in \mathcal{A}_{Y}^N$, each of length $N$ are **jointly typical** (to some tolerance $\beta$) over the distribution $P(x,y)$ *if*:
- $\mathbf{x}$ is typical of $P(\mathbf{x})$
- $\mathbf{y}$ is typical of $P(\mathbf{y})$
- $(\mathbf{x,y})$ is typical of $P(\mathbf{x,y})$


# Theorem 
Let $\mathbf{x},\mathbf{y}$ be drawn from $(XY)^N$ with $P(\mathbf{x},\mathbf{y})= \prod_{n}P(x_{n},y_{n})$
$\forall \beta >0$
- $P((\mathbf{x},\mathbf{y})\in J_{N_{\beta}}) \xrightarrow[n \to \infty]{}1$ (almost all pairs are jointly typical)

- $\lvert J_{N_{\beta}} \rvert\leq 2^{N(H(X,Y)+\beta)}$ (the number of jointly typical sequences is roughly RHS)

- For $\mathbf{x}'$, and $\mathbf{y}'$ drawn independently from the marginals of $P(\mathbf{x},\mathbf{y})$,                                           $P((\mathbf{x},\mathbf{y})\in J_{N_{\beta}})\leq 2^{-N(I(X;Y))-3\beta}$
The difference between the first and the third statement is that in the third statement relies on independence, so $p(x,y)=p(x)p(y)$. Those are very unlikely to be in $J$, but 