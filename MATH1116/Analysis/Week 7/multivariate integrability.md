Let $\prod_{j=1}^n \left[ a_{j},b_{j} \right]=R$, We denote this as the "rectangle"
We define $$1_{\prod_{j=1}^n [a_{j},b_{j}]} :\mathbb{R}^n \to \mathbb{R} \\x \mapsto \begin{cases}
1,\quad x \in {R} \\
0,\ \ \ \ \text{otherwise}
\end{cases}$$
Additionally, $\int_{\mathbb{R}^n}1_{\prod_{j=1}^n [a_{j},b_{j}]}(x)dx:= \prod_{j=1}^n \lvert b_{j}-a_{j} \rvert=:\int_{\prod_{j=1}^n [a_{j},b_{j}]}dx=: \int _{a_{n}}^{b_{n}}\dots\int_{a_{1}}^{b_{1}}dx_{1}\dots dx_{n}$

## Definition 2
Let $m \in \mathbb{N}$. Let $[a_{j,k},b_{j,k}]\subseteq \mathbb{R},$ where $j=1,\dots,n$ and $k=1,\dots,m$ and $\{ \alpha_{1},\dots,\alpha_{m} \}\in \mathbb{R}^m$
Then $$\int_{\mathbb{R}^n}\sum_{k=1}^m\alpha_{k}1_{\prod_{j=1}^n[a_{j,k},b_{j,k}]}(x)dx:=\sum_{k=1}^m \alpha_{k}\left( \prod_{j=1}^n \lvert  b_{j,k}-a_{j,k}\rvert  \right) $$
# Definition 3 (subrectangle)
Let $[a_{j},b_{j}]\subset \mathbb{R}\quad\forall j=1,\dots,n$
Let $M_{j}\in \mathbb{N}$, for $j=1,\dots,n$
Let $(a_{j,k})^{M_{j}}_{k=0}$ by such that $a_{j}=a_{j,0}<a_{j,1}<\dots<a_{j,M_{j}}=b_{j}$ for $j=1,\dots,n$

Some set of the form $\prod_{j=1}^n \left[ a_{j,k_{j}},a_{j,k_{j+1}} \right]$ for $k_{j}\in \{ 0,\dots,M_{j-1} \}$ is called a **sub rectangle** of $R$

# Definition 4 (partition)
The set of all subrectangles $\mathcal{P}$ is called a [[partition]] of $\prod_{j=1}^n [a_{j},b_{j}]$
Given $\delta>0$, $\mathcal{P}$ is a $\delta$-partition if $\forall R\in \mathcal{P}\quad\forall x,y\in R\ \lVert x-y \rVert<\delta$
