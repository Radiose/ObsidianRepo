The essence of a bisection argument is based off the nested interval theorem. 

Nested interval theorem:
In a [[Sequence]] of closed intervals $I_{n}=[a_{n},b_{{n}}]$, with $a_{n}\leq a_{n+1}$ and $b_{n+1}\leq b_{n}$ for all $n$, there is some $x$ which is in every interval $I_{n}$. This is essentially the same idea as the [[Bolzano Weierstrass theorem]].


The bisection argument is to prove that some $f$ thats [[continuous function|continuous]] on an interval $[a,b]$ with $f(a)>0$ and $f(b)<0$ that some $x \in[a,b]$ has $f(x)=0$.

We first prove that a nested interval $a_{n}$ and $b_{n}$ approach $x$ as $n \to \infty$ $a_{n} <x$ and similarly $b_{n}>x$
Now we show that $f(a_{n}) < 0$ in some neighbourhood, via [[Harder theorems for continuity]] no 3, and similarly for $f(b_{n})$.
We then prove via contradiction for clarity that $f(x)>0$ and then show that $f(a_{n})$ must then converge to some number $>0$. We prove this via the definition of [[Convergence of a sequence]], using the delta from the theorem 3 we showed previously. 

This contradicts that we know that $f(a_{n})>0$, thus $f(x)\leq 0$. We then do it similarly for $f(b_{n})$ and prove that $f(x) \geq 0$. Thus, $f(x)=0$.
