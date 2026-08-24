Given a [[basis]] $\alpha=\{ \alpha_{1},\dots,\alpha_{n} \}$ of $V$, we can define the dual basis of $\alpha$ is defined as $\{\phi_{1},\dots,\phi_{n}  \}$.


We define the function $\phi_{i}:V \to \mathbb{F}$ by $\phi_{i}(\alpha_{j})$ = 1 if $i = j$, $0$ else. 

For each $\phi_{i}$, we have defined $\phi$ on each element of a [[basis]]. So via, the [[basis of domain theorem]], we can extend it to the basis of a linear map.
$\{ \phi_{1},\dots,\phi_{n} \}$.

The overall idea here is the following. Suppose we have a vector
$v =2\alpha_{1}+5\alpha_{2}$, and we want to construct a [[function]] $f$ that does $f(\alpha_{1})=3$, $f(a_{2})=7$.
Then, for any $v =a_{1}\alpha_{1}+a_{2}\alpha_{2}$, we want $f(v)=3a_{1}+7a_{2}$
But, $\phi_{1}(v)=a_{1},\phi_{2}(v)=a_{2}$


Then, we can simply construct $f$ as $f=3\phi_{1}+7\phi_{2}$  because of linearity.
