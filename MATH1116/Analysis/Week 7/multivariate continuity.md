# vector valued  
A function $\mathbb{R}\to \mathbb{R}^n$ is said to be continuous at $x \in \mathbb{R}$ if 
$$\forall\epsilon>0 \quad \exists\delta >0\quad\forall y\in \mathbb{R} |x-y|<\delta \implies \lVert f(y)-f(x) \rVert<\epsilon  $$
## Theorem 1
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

# One dimensional codomain 

## Lemma 
Let $x,y\in \mathbb{R}^n,\lambda \in \mathbb{R}$

$(1)$ $\lVert x \rVert=0 \iff x=0$ 
$(2)\ \lVert \lambda x \rVert=\lvert \lambda \rvert\cdot \lVert x \rVert$
$(3)$ $\lVert x+y \rVert\leq \lVert x \rVert+\lVert y \rVert$
### Proof 
$(1)$,$(2)$ can be directly proven via the definition of a [[norm]]

$(3)$: $\lVert x+y \rVert^2=\langle x+y,x+y \rangle=\lVert x^2 \rVert+2 \langle x,y \rangle + \lVert y^2 \rVert$
$\leq \lVert x^2 \rVert + 2\lVert x \rVert\lVert y \rVert+\lVert y^2 \rVert$
$= (\lVert x \rVert+\lVert y \rVert)^2$

## Lemma 2
Let $(x_{j})_{j \in \mathbb{N}} \in (\mathbb{R}^n)^\mathbb{N}$
The following statements are equivalent 

$(1):$ $\exists x \in \mathbb{R}^n:\quad \lim_{ j \to \infty } \lVert x_{j}-x \rVert=0$ 

$(2): \forall k=1,..,n$ $(\langle x_{j},e_{_{k}} \rangle)$ is [[Cauchy sequence|cauchy]]

$(3):\ \ (x_{j})_{j \in \mathbb{N}}$ is Cauchy in $\mathbb{R}^n$

Proof:
exercise 


## Limit 

We say that $\lim_{ x \to x_{0} }f(x)=\ell$ if $\forall\epsilon >0 \quad \exists\delta>0\quad \forall y \in B(c,R)$, $\lVert y-x_{0} \rVert<\delta \implies \lvert f(x)-\ell \rvert<\epsilon$

## Continuous 
We say that $f$ is continuous at $x_{0}$ if $\lim_{ x \to x_{0} }f(x)=f(x_{0})$

We say that $f$ is continuous on a set $E \subset B(C,R)$ if $$\forall y \in E,\ \ \forall\epsilon>0\quad \exists\delta>0\quad\forall x,y \in E,\ \ \lVert x-y \rVert<\delta \implies \lvert f(x)-f(y) \rvert<\epsilon$$
## Uniformly continuous 

We say that $f$ is uniformly continuous on $E \subset B(C,R)$ if $$\forall\epsilon>0\quad\exists\delta>0\quad\forall x,y\in E,\quad\lVert x-y \rVert<\delta \implies \lvert f(x)-f(y) \rvert <\epsilon $$
