---
aliases:
  - integrable
---
Let $\prod_{j=1}^n \left[ a_{j},b_{j} \right]=R$, We denote this as the "rectangle"
We define $$1_{\prod_{j=1}^n [a_{j},b_{j}]} :\mathbb{R}^n \to \mathbb{R} \\x \mapsto \begin{cases}
1,\quad x \in {R} \\
0,\ \ \ \ \text{otherwise}
\end{cases}$$
Additionally, $\int_{\mathbb{R}^n}1_{\prod_{j=1}^n [a_{j},b_{j}]}(x)dx:= \prod_{j=1}^n \lvert b_{j}-a_{j} \rvert=:\int_{\prod_{j=1}^n [a_{j},b_{j}]}dx=: \int _{a_{n}}^{b_{n}}\dots\int_{a_{1}}^{b_{1}}dx_{1}\dots dx_{n}$

## Definition 2
Let $m \in \mathbb{N}$. Let $[a_{j,k},b_{j,k}]\subseteq \mathbb{R},$ where $j=1,\dots,n$ and $k=1,\dots,m$ and $\{ \alpha_{1},\dots,\alpha_{m} \}\in \mathbb{R}^m$
Then $$\int_{\mathbb{R}^n}\sum_{k=1}^m\alpha_{k}1_{\prod_{j=1}^n[a_{j,k},b_{j,k}]}(x)dx:=\sum_{k=1}^m \alpha_{k}\left( \prod_{j=1}^n \lvert  b_{j,k}-a_{j,k}\rvert  \right) $$
# Definition 3 (sub rectangle)
Let $[a_{j},b_{j}]\subset \mathbb{R}\quad\forall j=1,\dots,n$
Let $M_{j}\in \mathbb{N}$, for $j=1,\dots,n$
Let $(a_{j,k})^{M_{j}}_{k=0}$ by such that $a_{j}=a_{j,0}<a_{j,1}<\dots<a_{j,M_{j}}=b_{j}$ for $j=1,\dots,n$

Some set of the form $\prod_{j=1}^n \left[ a_{j,k_{j}},a_{j,k_{j+1}} \right]$ for $k_{j}\in \{ 0,\dots,M_{j-1} \}$ is called a **sub rectangle** of $R$

So, for each dimension $j$, we create some number of "cuts" $M_{j}$, and then from there we can create a sub rectangle by selecting two consecutive cuts in each dimension. 


# Definition 4 (partition)
The set of all sub rectangles $\mathcal{P}$ is called a [[partition]] of $\prod_{j=1}^n [a_{j},b_{j}]$
Given $\delta>0$, $\mathcal{P}$ is a $\delta$-partition if $\forall R\in \mathcal{P}\quad\forall x,y\in R\ \lVert x-y \rVert<\delta$
(no 2 points in any rectangle are more than $\delta$ from each other)
We also call this the *mesh size*

# Definition 5 (refinement)
We call $Q$ a refinement of $\mathcal{P}$ if:
$$\forall R' \in Q\ \exists!R \in \mathcal{P}\quad R' \subset R$$
We notate this as $Q \lessdot \mathcal{P}$

# Definition 6 (selection)
A function $x:\mathcal{P}\to \prod_{j=1}^n [a_{j},b_{j}]$ such that $\forall R \in \mathcal{P}\quad x(R)\in R$ is called a selection.

The set of all selections over $\mathcal{{P}}$ is denoted $S(\mathcal{P})$

Let $f: \prod_{j=1}^n [a_{j},b_{j}] \to \mathbb{R}$

Then, $\sum_{R \in \mathcal{P}}f(x(R))\left( \int_{R}dx \right)$ is a [[Riemann sum]]

# Integrable 

$f$ is called integrable if $$
\exists L\quad\forall\epsilon>0\quad\exists \delta\quad \forall \mathcal{P}\ \delta \text{-partition}\quad\forall x \in S(Q)\\ \\
\left\lvert  \sum_{R \in Q}f(x(R))\left( \int_{R}dx \right)-L  \right\rvert<\epsilon $$
We write $\int_{\prod_{j=1}^n [a_{j},b_{j}]}f(x)dx:=L$
# Proposition 
Let $f,g: \prod_{j=1}^n [a_{j},b_{j}] \to \mathbb{R}$ and $\lambda \in \mathbb{R}$
Then, $\int_{\prod_{j=1}^n[a_{j},b_{j}]}f(x)+\lambda g(x)= \int_{\prod_{j=1}^n}f(x)dx+\lambda \int_{\prod_{j=1}^n}g(x)dx$

# Upper and lower Riemann sums 
Let $f:\prod_{j=1}^n[a_{j},b_{j}]\to \mathbb{R}$ be [[continuous function|continuous]]
Let $\mathcal{P}$ be a [[partition]]
$\bar{S}(\mathcal{P})=\sum_{R\in \mathcal{P}}\sup_{x \in\mathbb{R}}f(x)\left( \int_{R}dx \right)$ - an upper Riemann sum (the largest point in each sub rectangle)
$\underline{S}=\sum_{R \in \mathcal{P}}\inf_{x \in R}f(x)\left( \int_{R}dx \right)$ - the lower Riemann sum
