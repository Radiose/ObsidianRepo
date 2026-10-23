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

## Upper and lower Riemann sums 
Let $f:\prod_{j=1}^n[a_{j},b_{j}]\to \mathbb{R}$ be [[continuous function|continuous]]
Let $\mathcal{P}$ be a [[partition]]
$\bar{S}(\mathcal{P})=\sum_{R\in \mathcal{P}}\sup_{x \in\mathbb{R}}f(x)\left( \int_{R}dx \right)$ - an upper Riemann sum (the largest point in each sub rectangle)
$\underline{S}=\sum_{R \in \mathcal{P}}\inf_{x \in R}f(x)\left( \int_{R}dx \right)$ - the lower Riemann sum



# Lemma 
Let $f:\prod_{j=1}^n[a_{j},b_{j}] \to \mathbb{R}$ be continuous. 
Let  $\epsilon>0$, let $\delta>0$. Let $\mathcal{P}$ be a $\delta$ partition of $\prod_{j=1}^n[a_{j},bj]$ and $\mathcal{Q}$ be a refinement of $\mathcal{P}$
Then, $$\bar{S}(\mathcal{Q})\leq \bar{S}(\mathcal{P})\leq\bar{S}(Q)+2\epsilon \prod_{j=1}^n \lvert b_{j}-a_{j} \rvert$$

### Proof 
Note that $f$ is uniformly continuous, as it is continuous on a closed, compact set.
IE $$\forall\epsilon >0\quad\exists \delta >0\quad \forall x,y \in \prod_{j=1}^n[a_{j},b_{j}]\quad \lVert x-y \rVert<\delta \implies |f(x)-f(y)|<\epsilon$$Let $\epsilon>0$, and let $\delta$ be as above. Let $\mathcal{P}$ be a $\delta$ partition, and $\mathcal{Q}\lessdot\mathcal{P}$
$$\bar{S}(\mathcal{Q})= \sum_{R' \in \mathcal{Q}}\sup_{x \in R'}  f(x) \left( \int_{R'}dx \right) \\ = \sum_{R \in \mathcal{P}}\sum_{R' \in Q\\ R' \subset R} \sup_{x \in R'}{f(x) \left( \int_{R'}dx \right)} \text{ rewriting/grouping}\\ \leq \sum_{R \in \mathcal{P}}\sum_{R' \in\mathcal{Q} \\ R' \subset R} \sup_{x \in R}{f(x) \left( \int_{R'}dx \right) }\\ =\sum_{R \in \mathcal{P}}\sup_{x \in R}f(x) \left[ \sum_{R' \in Q \\ R' \subset R}\left( \int_{R'}dx \right)  \right] \text{\ sup of R doesnt depend on R'}\\ =\sum_{R \in \mathcal{P}}\sup_{x \in R}f(x)\left( \int_{R}dx \right)=\bar{S}(\mathcal{P})$$
Now, 
$$\bar{S}(\mathcal{Q})=\sum_{R' \in \mathcal{Q}} \sup_{x \in R'}f(x)\left( \int_{R'}dx \right)\\= \sum_{R \in \mathcal{P}}\sum_{R' \in Q \\ R'\subset R} \sup_{x \in R'} f(x)\left( \int_{R'}dx \right) \\ \geq \sum_{R \in \mathcal{P}}\sum_{R' \in \mathcal{Q}} \sup_{x \in R}(f(x)-\epsilon)\left( \int_{R'}dx \right)$$
This final inequality is the tricky part. Because, we know that 

$$\sum_{R \in \mathcal{P}}\sum_{R' \in Q\\ R' \subset R} \sup_{x \in R'}{f(x) \left( \int_{R'}dx \right)}  \leq \sum_{R \in \mathcal{P}}\sum_{R' \in\mathcal{Q} \\ R' \subset R} \sup_{x \in R}{f(x) \left( \int_{R'}dx \right) }$$and that because $\mathcal{P}$ is an $\delta$ sufficient subset, 

$\sup_{x \in R'}f(x)\geq \sup_{y \in R}f(y)-\epsilon$

This is further shown below

How is $\epsilon$ obtained?
For $x \in R' \subset R$
$\lVert x-y \rVert<\delta \implies \lvert f(x)-f(y) \rvert<\epsilon$
$\implies f(x)\geq f(y)-\epsilon$ from uniform continuity

$$=\bar{S}(\mathcal{P})-\epsilon \left( \sum_{R \in \mathcal{P}}\sum_{R' \in Q} \left( \int_{R'}dx \right) \right)=\bar{s}(\mathcal{P})-\epsilon \prod_{j=1}^n[a_{j}-b_{j}]$$
# Theorem 
If $f: \prod_{j=1}^n[a_{j},b_{j}] \to \mathbb{R}$ is continuous, then it is integrable.

### Proof 
Define $L = \inf_{}{\bar{S}(\mathcal{P}):\mathcal{P}\text{ is a partition of }\prod_{j=1}^n [a_{j},b_{j}]}$
Let $\epsilon >0$. Choose $\delta >0$ such that $$\forall x,y \in \prod_{j=1}^n[a_{j},b_{j}],\quad \lVert x-y \rVert<\delta \implies \lvert f(x)-f(y) \rvert<\epsilon$$Then pick $\mathcal{P}_{\epsilon}$ such that $L\leq \bar{S}(P_\epsilon)\leq L + \epsilon$
Pick $\delta$ as in the [[multivariate integrability#Lemma|lemma]] and pick $\mathcal{P}$ as a $\delta$ partition. 
Take $\mathcal{Q_{\epsilon}}$ as a $\delta$ partition such that $\mathcal{Q}\lessdot \mathcal{P}$ and $\mathcal{Q}_{\epsilon} \lessdot \mathcal{P}_{\epsilon}$
Let $x \in S(\mathcal{Q}_{\epsilon})$
Then $$\sum_{R \in \mathcal{P}}f(x(R))\left( \int_{R}dx \right)-L \\ \leq \bar{S}(\mathcal{P})-L \leq \bar{S}(\mathcal{Q}_{\epsilon})+\epsilon \prod_{j=1}^n|a_{j}-b_{j}|-L\text{ via the lemma} \\ \leq \bar{S}(\mathcal{P}_{\epsilon})+\epsilon\prod_{j=1}^n|b_{j}-a_{j}|-L \leq \left( 1+ \prod_{j=1}^n \lvert b_{j}-a_{j} \rvert \right)\epsilon $$
Now the other direction 
$$\sum_{R \in \mathcal{P}}f(x(R))\left( \int_{R}dx \right)\geq \bar{S}(\mathcal{P})-\epsilon \prod_{j=1}^n \lvert b_{j}-a_{j} \rvert -L \text{ uniform continuity, the sup is within epsilon of any point}\\\geq \bar{S}(\mathcal{Q}_{\epsilon})-\epsilon\prod_{j=1}^n|b_{j}-a_{j}|-L\text{ by the lemma} \\ \geq \bar{S}(\mathcal{P}_\epsilon)-2\epsilon\prod_{j=1}^n|b_{j}-a_{j}| -L \geq -2\epsilon \prod_{j=1}^n|b_{j}-a_{j}|-L\text{ by the choice of }\bar{S}(\mathcal{P}_{\epsilon}) \blacksquare$$
	

# Theorem 2 
Let $f:[a,b]\times[c,d] \to \mathbb{R}$ be continuous.
Define $$F:[c,d] \to \mathbb{R}\\y \mapsto \int_{a}^b f(x,y)dx\\ \\G:[a,b]\to \mathbb{R}\\x \mapsto \int_{a}^b f(x,y)dy$$
Then $\int f(z)dz=\int_{c}^d F(y)dy=\int_{a}^b G(x)dx=\int_{c}^d (\int_{a}^b f(x,y)dy$


