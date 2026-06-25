Let $c_{n}$ be a [[Sequence]] of [[real number]]s all of which are contained in the closed bounded interval $[a,b]$.
Then, some [[subsequence]] exists that [[Convergence of a sequence|converges]], and the [[limits|limit]] also belongs to $[a,b]$

Note that this theorem only applies closed intervals. For example, $[0,\infty)$ does not apply to this theorem. 

### Idea of proof
We divide the interval $[a,b]$ into two subintervals, each equal length and a common endpoint being the midpoint. We keep one subinterval (which will contain an infinite [[subsequence]] of $c_{n}$). We then divide this subinterval again and again, keeping one half, until we eventually define a new subsequence of the original interval such that $x_{n}$ is the $n$th subinterval.

## Formally
Let $c_{n}$ be a [[Sequence]] of [[real number]]s all of which are contained in the closed bounded interval $[a,b]$.

Divide the interval $[a,b]$ into two closed, bounded intervals $\left[ a, \frac{a+b}{2} \right]$ and $\left[ \frac{a+b}{2}, b \right]$ with equal length and common endpoint $\frac{a+b}{2}$. At least one of these subintervals contain an infinite (given) subsequence of the original sequence. We choose one of these and denote it $[a_{1},b_{1}]$. 

Similarly, we subdivide $[a_{1},b_{1}]$ and choose a subinterval that contains an infinite subsequence of the original sequence. We choose one of these and denote it $[a_{2},b_{2}]$. etc etc.

Now we define a subsequence that [[Convergence of a sequence|converges]] $x_{n}$ from the original sequence as follows. Choose some $x_{1}$ from the subinterval $[a_{1},b_{1}]$. Then some $x_{2}$ from $[a_{2},b_{2}]$ that occurs after the 
