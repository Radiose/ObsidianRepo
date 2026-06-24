Its normally pretty inefficient to use the [[limits|limit]] definition to prove [[Convergence of a sequence]].
There are a number of theorems that will be used instead. 



## Basic properties 
Suppose $\lim_{ } a_{n} = a$,  $\lim_{ }b_{n}=b$
Then 
(6)$\lim_{ }(a_{n}\pm b_{n}) = (a+b)$
(7)$\lim_{  }c \cdot a_{n}=c \cdot a$
(8)$\lim_{  }a_{n}b_{n}=ab$
(9)$\lim_{  } \frac{a_{n}}{{b_{n}}}=\frac{a}{b}$ (assuming $b \not=0$)
Note that (9) implies that ultimately $b_{n} \not=0$ 

proof of 6:
(+) case 
Suppose $a_{n} \to a$ and $b_{n} \to b$. Let $\epsilon > 0$. Since $a_{n} \to a$, there an integer $N_{1}$ such that 
$n > N_{1} \implies |a_{n}-a|<\frac{\epsilon}{2}$
Since $b_{n} \to b$, then similarly $\exists N_{2}$
$n > N_{2} \implies |b_{n}-b|< \frac{\epsilon}{2}$
It follows then that if $N = Max\{ N_{1},N_{2} \}$
then 
$|(a_{n}+b_{n})|=|(a_{n}-a)+(b_{n}-b)|$
$< |a_{n}-a|+|b_{n}-n|$ via triangle inequality 
< $\epsilon$


Proof of 7:
Suppose $a_{n} \to a$
We aim to show that $|ca_{n}-ca|<\epsilon$ for all sufficiently large $n$ 
Since $a_{n} \to a$, $\exists N \in \mathbb{Z}$ such that $n > N \implies |a_{n}-a|< \frac{\epsilon}{|c|}$ 
Multiplying both sides of the inequality by $|c|$ shows that  
$|c||a_{n}-a|<\epsilon$
$\iff |ca_{n}-ca|<\epsilon$
and thus $ca_{n} \to c$

Proof of 8:
Suppose $a_{n} \to a$ and $b_{n} \to b$. Let $\epsilon>0$, 
then $\exists N \in \mathbb{Z}$ s.t $|a_{n}b_{n}-ab|$ 
$= |a_{n}b_{n}-a_{n}b+b_{n}a -ab| = |a_{n}(b_{n}-b)+b(a_{n}-a)|$
$\leq |a_{n}(b_{n} -b)|+|b_{n}(a_{n}-a)|$ via triangle inequality 
$= |a_{n}||b_{n}-b|$ + $|b||a_{n}-a|$
We now show that each term is $< \frac{\epsilon}{2}$ (for sufficiently large n)
For the second term, this is true when $b=0$, as the term is zero.
When $b \not=0$, since $a_{n} \to a$, then we can choose $N_{1}$ such that 
$$|a_{n}-a|< \frac{\epsilon}{2|b|} \text{ for all } n > N_{1}$$
And so, $|b||a_{n}-a|< \frac{\epsilon}{2}$ for all $n > N_{1}$ 

For the first term, we use theorem 3 (below) to deduce that $M |b_{n}-b|< \frac{\epsilon}{2}$
Thus, 
$|a_{n}||b_{n}-b| < \frac{\epsilon}{2} \text{ for all }  n < N_{2}$
Hence, $|a_{n}b_{n} - ab|<\epsilon$ for all $n > N$ where $N = max\{N_{1},N_{2}\}$



# Other theorems
Theorem 1:
If two [[Sequence]]s converge, then so does their sum, and the limit of the new sequence is just the sum of the limits of the original sequence. 
Similar results apply for all products and quotients. 

Theorem 2: 
Suppose $\lim_{ } a_{n} = a$ and $\lim_{ }a_{n} = b$, then $a = b$
Two methods to prove, both via contradiction. The first can be done geometrically, by fixing $\epsilon$ to some value related to the distance between $a$ and $b$, as $a \not=b$ (via contradiction).  The other method is to algebraically manipulate via the triangle [[Inequality]].





Theorem 3:
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

Proof:
we utilise a similar proof to that done for theorem 1 
Suppose $a_{n} \to a$, $b_{n} \to b$, and $a_{n} \le b_{n}$ ultimately.
Assume $a>b$. Let $\epsilon = \frac{1}{3}(a-b)$
Then $a_{n} \in (a-\epsilon, a+\epsilon)$ ultimately. 
In particular 
$a_{n} > a-\epsilon$.
Similar, $b_{n} \in b+\epsilon$ ultimately 
Since $\epsilon = \frac{1}{3}(a-b)$, then this implies $a_{n}>b_{n}$ ultimately.
![[Pasted image 20260623193537.png]]

This image above can show this. 

This contradicts $a_{n} \leq b_{n}$ and so the assumption is false. Thus, $a \le b$.






![[squeeze theorem]]


## Bounded sequences 

If a sequence is bounded and ultimately monotone, then it converges. 

We use the [[Completeness axiom]] to prove.

For the ultimately decreasing case:
Suppose the sequence $a_{n}$ decreases from the $N$th term onwards. Considering terms from this point, we get a sequence $a_{N}, a_{N+1}\dots a_{n}$. This set is bounded below, and thus, via the completeness axiom, this set has a greatest lower bound we denote $L$. We will prove that $\lim a_{n} = L$. 

Suppose $\epsilon > 0$. Because $L$ is a lower bound, then $L \leq a_{n}$ for all $n$.
Because $L$ is the greatest lower bound, then $L+\epsilon$ is not a lower bound, and so there is a $k \in \mathbb{Z}$ such that $a_{k} < L+\epsilon$ 

Because this [[Sequence]] is constantly decreasing, then $a_{n}<L+\epsilon$ for all $n \geq k$
Thus, we have shown that $L \leq a_{n} \leq L+\epsilon$ for all $n \geq k$ ($k$ depends on $\epsilon$)
Since $\epsilon$ is arbitrary, $a_{n}\to L$ while $n \to \infty$
