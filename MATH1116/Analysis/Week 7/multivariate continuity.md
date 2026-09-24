## Single dim domain 
A function $\mathbb{R}\to \mathbb{R}^n$ is said to be continuous at $x \in \mathbb{R}$ if 
$$\forall\epsilon>0 \quad \exists\delta >0\quad\forall y\in \mathbb{R} |x-y|<\delta \implies \lVert f(y)-f(x) \rVert<\epsilon  $$
# Theorem 1
Let $f:\mathbb{R}\to \mathbb{R}^n$. Define, for $j=1,\dots,n$, 
$x_{j}:\mathbb{R}\to \mathbb{R}$
$t \mapsto f(t)\cdot e_{j}$, where $e_{j}$ is a part of the [[canonical basis]] ([[inner product|dot product]]).

$f$ is [[continuous function|continuous]] at $t\in \mathbb{R}$ if and only if $x_{j}$ is continuous at $t$ for all $j=1,\dots,n$
### Proof 
$\implies$
Let $t \in \mathbb{R}$
Assume that $\forall\epsilon>0\quad \exists\delta>0\quad\forall  \in\mathbb{R} \quad |t-s|<\delta \implies \lVert f(t)-f(s) \rVert<\epsilon$
Let $j =1,..,n$, $\epsilon>0$ and $\delta$ be as above. Let $|t-s|<\delta$
Recall that $|x_{j}-x_{t}|=|f(t)e_{j}-f(s)e_{j}|\leq \sum_{k=1}^n |(f(t)-f(s))e_{k}| =\lVert f(s)-f(t) \rVert<\epsilon^2$
$\impliedby$
Assume $\forall j\in \{ 1,..,n \}\quad\forall\epsilon>0\quad\exists\delta_{j}>0$ such that $\forall x \in \mathbb{R}$
$|t-s|<\delta_{j} |x_{j}(t)-x_{j}(s)|<\epsilon$
let $\epsilon>0$. Pick $\delta=min \{ \delta_{j=1},\dots,\delta_{j=n} \}$
Assume $|t-s|<\delta$
then, $|t-s|<\delta_{j}\forall j \in \{ 1,\dots,n \}$
thus, $|x_{j}(t)-x_{j}(s)|<\epsilon$
$\sum_{j=1}^n \lvert x_{j}(t)-x_{j}(s) \rvert^2 <n\cdot\epsilon^2$
$\implies \lVert f(t)-f(s) \rVert<\sqrt{ n }\epsilon$
$\blacksquare$
