uniform continuity

This is a specific property of a continuous function defined by the following statement 
$\forall\epsilon\ \exists \delta \ \ s.t\ \ \forall x,y \in A$
$|x-y|<\delta \implies|f(x)-f(a)|<\epsilon$

To rigorously prove, we need a tool to help us to do this. 

Suppose that we have two intervals, $[a,b], \ [b,c]$ with a function $f$ continuous on $[a,c]$. Let $\epsilon >0$ and suppose that the following statements hold 

if $x$ and $y$ are in $[a,b]$ and $|x-y|<\delta_{1}$, then $|f(x)-f(y)|<\epsilon$
if $x$ and $y$ are in $[b,c]$ and $|x-y|<\delta_{2}$, then $|f(x)-f(y)|<\epsilon$
We would like to know if theres some $\delta>0$ such that $|f(x)-f(y)|<\epsilon$ whenever $x,y$ are points in $[a,c]$ with $|x-y|<\delta$