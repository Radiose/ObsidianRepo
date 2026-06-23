Its normally pretty inefficient to use the [[limits|limit]] definition to prove [[Convergence of a sequence]].
There are a number of theorems that will be used instead. 

Theorem 1:
If two [[Sequence]]s converge, then so does their sum, and the limit of the new sequence is just the sum of the limits of the original sequence. 
Similar results apply for all products and quotients. 

Suppose $\lim_{ } a_{n} = a$,  $\lim_{ }b_{n}=b$
Then 
(6)$\lim_{ }(a_{n}\pm b_{n}) = (a+b)$
(7)$\lim_{  }c \cdot a_{n}=c \cdot a$
(8)$\lim_{  }a_{n}b_{n}=ab$
(9)$\lim_{  } \frac{a_{n}}{{b_{n}}}=\frac{a}{b}$ (assuming $b \not=0$)
Note that (9) implies that ultimately $b_{n} \not=0$ 


Theorem: 
Suppose $\lim_{ } a_{n} = a$ and $\lim_{ }a_{n} = b$, then $a = b$
Two methods to prove, both via contradiction. The first can be done geometrically, by fixing $\epsilon$ to some value related to the distance between $a$ and $b$, as $a \not=b$ (via contradiction).  We then 




Theorem:
Suppose $a_n = a$, then the sequence is bounded, that is, there is a [[real number]] $M$ such that $|a_{n}|<M$ for all $n$

Proof:
let $\epsilon =1$
Thus, via the definition of convergence, $\forall\epsilon >0 \exists N \in \mathbb{Z}\ \ \ \ n > N \implies |a_{n}-a| < \epsilon$
$\iff a-1 < a_{n} < a+1$
We fix N, thus we have a finite set of terms $\{ a_{1},a_{2}\dots a_{N} \}$. Because it is finite, there must exist real numbers $M_{1}$ and $M_{2}$ such that $M_{1} \le a_{n} \le M_{2}$ for all $n \leq N$.
let $M = max \{ M_{1},M_{2}\}$
Thus, $|a| \leq M$




[[theorem]]:
Suppose $a_{n} \to a$, $b_{n} \to b$, and $a_{n} \le b_{n}$ ultimately. Then, $a \le b$
Note that this does not work for strictly $<$




![[squeeze theorem]]
