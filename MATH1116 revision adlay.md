Worksheet knowledge from each question:

Analysis:
W5:
Determine $f_{n}(x)= n\exp(-nx)$ converges uniformly 
Because integral limits commuting is a necessary condition for uniform convergence, proving that they dont means that $f_{n}$ must converge uniformly - could also work with continuous functions 

W6:
Determine whether a series of functions converges uniformly
Idea: utilise integration by parts - comparison test - if the sup norm of the thing converges, then the series converges 



W7:
Show that a series of functions that converges uniformly have its derivative converge uniformly:
Proof idea:






Sequence of functions:
Pointwise convergence:
$\forall x \in \mathbb{R}\quad\forall\epsilon>0\quad \exists N \in \mathbb{N}$ such that $\forall n > N\quad |f_{n}(x)- f(x)|<\epsilon$
Problems: 
integral doesnt commute with limit 
doesnt imply continuity of limit 
limits cannot be exchanged



Uniform convergence 
$\forall\epsilon>0 \quad \exists N\quad \forall n>N\quad \lVert f_{n}-f \rVert_{\infty}<\epsilon$
So difference is that this doesnt depend on x.

Uniformly cauchy:
$\forall\epsilon \quad \exists N\in \mathbb{N}\quad \forall n,m >N\quad \lVert f_{n}-f_{m} \rVert_{\infty} <\epsilon$
if you prove uniformly cauchy, you can prove uniform convergence. 


Very important.
-All t eventually pass N at some point 
Allows for: exchange of limits
the integral of a limit is the limit of the integral 
the limit of a continuous sequence of functions is also continuous 

Theorems: Integral limit 
Requires continuous $f_{n}$
Proven, because the difference between the two is less than the integral of the sup norm, which is a constant, so then as N approaches infinity that constant goes to 0.

Limit is continuous:
Remember the goal is to prove $\forall x \in [a,b]\quad \forall\epsilon>0\quad \exists\delta>0 \quad \lvert x-y \rvert<\delta \implies \lvert f(x)-f(y) \rvert<\epsilon$
We know that $\forall n \in \mathbb{N}, \forall x \in[a,b]\quad\dots|x-y|\delta \implies |f_{n}(x)-f_{n}(y)|<\epsilon$
So we use that, add in the $f_n(x)$ and y to the actual inequality, and from there we can control because $f_{n}-f$ is less than the sup norm ( which is less than epsilon chosen at the beginning)
Note that this also 





Power series:
Require uniform convergence to be created. The idea is that $f_{N}(x)=\sum_{n=1}^N a_{n}(x-c)^n$ converges uniformly to $f(x)$ when $x$ is in the radius of convergence 

Theorems:
ROC one 

lim $\frac{a_{n+1}}{a_{n}}$ is the inverse of the ROC. If it = 0, then ROC is $\mathbb{R}$, if it equals $\infty$, then $ROC$= 0


Derivative and integral have same ROC 

Built using $\frac{f^n(c)}{n!}$ as $a_{n}$


Requires 




LA:
COORDINATING MATRICES


Annihilator: $ann(u)=\{ \phi \in V^V | \phi(u)=0 \forall u\in V \}$
$ann(ann(u))=u$
$\ker(T^v)=ann(range(T))$
$range(T^v)=ann(\ker(T))$
$\dim(\ker(T^V))=\dim(W)-\dim(V)+\dim\ker(T)$
