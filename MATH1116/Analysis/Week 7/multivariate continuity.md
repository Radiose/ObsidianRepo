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

We say that $f$ is [[uniform continuity|uniformly continuous]] on $E \subset B(C,R)$ if $$\forall\epsilon>0\quad\exists\delta>0\quad\forall x,y\in E,\quad\lVert x-y \rVert<\delta \implies \lvert f(x)-f(y) \rvert <\epsilon $$

# Proposition 
Let $c \in \mathbb{R}^n$, let $f,g:B(c,R)\to \mathbb{R}^n$ be continuous at $x \in B(c,R)$ and $\lambda \in \mathbb{R}$.
Then,
- $f+\lambda g$ is continuous at $x$
- $f \cdot g$ is continuous at $x$
- if $\exists R_{0}>0| \ g(y)\not=0\ \ \forall y \in B(x,R_{0})$, then $\frac{f}{g}$ is continuous at $x$
- for $h \in C(\mathbb{R},\mathbb{R}),\ f(h)$ is continuous on $B(c,R)$.

## Proposition 2 
The functions $p_{j}:\mathbb{R}^n \to \mathbb{R}$ such that $p_{j}(x_{1},\dots,x_{n})=x_{j}$ are continuous on $\mathbb{R}^n$
### Proof 
note first that $p_{k}(x)=x_{k}=\langle x,e_{{k}} \rangle$
let $x_{0}\in \mathbb{R}^n$, Let $k \in \{ 1,\dots,n \}$
$\lvert \langle x,e_{k} \rangle-\langle x_{0},e_{k} \rangle \rvert= \lvert \langle x-x_{0},e_{k} \rangle \rvert$
$\leq \lVert x-x_{0} \rVert\cdot \lVert e_{k} \rVert$ (via [[Cauchy-schwarz inequality]])
$= \lVert x-x_{0} \rVert$
Thus, we have that $\forall \epsilon>0\ \ \forall x \in \mathbb{R}^n,\ \lVert x-x_{0} \rVert<\epsilon \implies \lvert p_{n}(x)-p_{n}(x_{0}) \rvert<\epsilon$

## Remark
Note that if $T:\mathbb{R}^n \to \mathbb{R}$ is [[linear map|linear]], then T is continuous. 
This is because any element of the [[dual vector space]] is a linear combination of $p_{k}$ functions shown above. A linear combination of continuous functions is continuous. 

# Theorem 
Let $[a_{j},b_{j}]\subset \mathbb{R}$, $j=1,\dots,n$ and $$E:= \prod_{j=1}^n [a_{j},b_{j}]:=\{ x \in \mathbb{R}^n:a_{j}\leq x_{j}\leq b_{j}\forall j=1,\dots,n \}$$If $f:E\to \mathbb{R}$ is continuous on $E$, then it is uniformly continuous and bounded on $E$. 
### Proof 
Assume $f$ is not uniformly continuous, so $$\exists\epsilon>0\ \forall\delta>0 \exists x,y\in E^{\mathbb{N}^*}\ \ \lVert x-y \rVert<\delta \land \lvert f(x)-f(y) \rvert \geq \epsilon $$Then, $$\exists(x_{m})_{m \in \mathbb{N}},\ (y_{m})_{m \in \mathbb{N}} \in E^{\mathbb{N}^*}\quad \lVert x_{m}-y_{m} \rVert< \frac{1}{m} \land \lVert f(x_{m})-f(y_{m}) \rVert\geq \epsilon$$
We are building two sequences, from the pair of points that is given by $\delta=\frac{1}{m}$.
For $j=1,\dots,n$, we have that $\langle x_{m},e_{j} \rangle_{m \in \mathbb{N}}\in[a_{j},b_{j}]^{\mathbb{N}^*}$ has a converging subsequence, via the [[Bolzano Weierstrass theorem]] in $\mathbb{R}$, so each vector value converges within $x_{m}$. Our goal from here is to create the overall sequence such that all of the vector values converge. 

The sequence, in $x_{m}\cdot e_{1}$ has a convergent subsequence, via BWT, so we extract the subsequence $m_{i},\dots,m_{n}$ that converges. Then, we put these on $x_{m}\cdot e_{2}$ and get the convergent subsequence of that, and repeat $n$ times. This gives us $m_{k} \in (\mathbb{R}^\mathbb{N})^n$



This gives us that $\exists (m_{k})_{k \in \mathbb{N}}\in \mathbb{N}^\mathbb{N}$ increasing and $x \in E$ such that $$\lvert x \cdot e_{j}-x_{m_{k}}\cdot e_{j} \rvert \xrightarrow[k \to \infty]{}0 \quad \forall j=1,..,n $$
