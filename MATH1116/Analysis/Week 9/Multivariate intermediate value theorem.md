Let $c \in \mathbb{R}^n$, $R>0, \ \ x,y\in B(c,R)$. Let $f:B(c,R) \to \mathbb{R}^n$ be continuous, and $f(x)<f(y)$. 
Let $v \in[f(x),f(y)]$. Then $\exists z \in B(c,R)$ such that $f(z)=v$

### Proof 
The first part of this proof is establishing that the the [[open ball]] is [[convex set|convex]]. This means that a straight line between two points in the open ball is contained completely within the open ball.

Remark that $\forall t\in [0,1]$,$$\lVert x+t(y-x)-c \rVert =\lVert (1-t)x+ty-(1-t)c-tc \rVert \newline\newline \leq(1-t)\lVert x-c \rVert+t\lVert y-c \rVert\newline\newline\leq (1-t)R+tR=R $$Part 2:
Define $h:[0,1] \to \mathbb{R}$
	$t \mapsto f(x+t(y-x))$
Then, $\forall t, s \in[0,1]$
Since $\lVert[(x+t(y-x)] -\left[ x+ s(y-x)\right]\rVert\leq \lvert t-s \rvert\ \lVert y-x \rVert$

$\lvert t-s \rvert<\delta \implies \lVert[(x+t(y-x)] -\left[ x+ s(y-x)\right]\rVert<\delta R$ 
This shows that the composition of $f$ and $x+t(y-x)$ is continuous, thus making $h$ continuous. 
We have that $h(0)=f(x)<f(y)=h(1)$,
We can then use the single variate [[intermediate value theorem]], and show that $$\forall v\in[h(0),h(1)]\quad \exists t_{0}\in[0,1]:h(t)=v\blacksquare$$
