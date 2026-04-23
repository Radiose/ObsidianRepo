The fundamental [[theorem]] of calculus

two parts:

If $f,F$ are [[Function]]s defined on (a,b), then we say that F is an **antiderivative** of f on (a,b) if $F'(x) = f(x)$ for all x $\in (a,b)$

[[theorem]]

i: Let g : $[a,b] \to \mathbb{R}$ be the [[Function]] g(x) = $\int_{a}^x f(t)dt$. Then g is an antiderivative of f on (a,b).

ii: If F is [[continuous function|continuous]] on \[a,b] and an antiderivative of f on (a,b), then $\int_{a}^b f(x)dx = F(b)-F(a)$

there may be(usually almost always are) many antiderivatives for a [[Function]].


## Proof of [[The fundamental theorem of calculus]] 
The essence of the fundamental theorem of calculus is that integration and differentiation are inverses that undo each other. So the area under a curve is the inverse of the instantaneous rate of change. The beauty of this is that before this fundamental theorem, integration is treated as a [[Riemann sum]]. This [[theorem]] shows how [[Derivative]]s and [[Definite integral]]s are intrinsically linked. 

### as explained in the course 

Suppose that a, b are real numbers such that a < b and f is a function that
is continuous on an interval \[a, b]. Let F be a function that is continuous
on \[a, b] and such that F' = f at all points in (a, b).

(F is the [[Indefinite integral|antiderivative]] of f)

For each positive integer n, we construct a [[partition]] $P_{n}$ and an associated
set of sample points $S_{n}$ as follows. Let $P_{n} = (x_{0}, x_{1}, x_{2},\dots , x_{n})$ be the
regular partition of \[a, b] with $\Delta x = \frac{b-a}{n}$ and $x_{i}=a+i\Delta x$

($\Delta x$ is the width of the [[partition]], n is the amount of subintervals)

Since F is differentiable on \[a,b], we may apply [[The mean value theorem]] on each subinterval $[x_{i-1},x_{i}]$. 

$\exists _c f'(c) =\frac{f(b)-f(a)}{b-a}$
thus 
$F'(x_{i}^*)=\frac{F(x_{i})-F(x_{i-1})}{x_{i}-x_{i-1}}$
The mean value point states that there is some point within the interval where the rate of change is equal to the average of the two points. This is useful, as it shows that a star point exists. 

therefore, 
$F(x_{i})-F(x_{i-1})=F'(x_{i}^*)(x_{i}-x_{i-1})=f(x_{i}^*)\Delta x$
This has given us a very useful statement. The difference between the intervals of the [[Indefinite integral|antiderivative]] of x has given us basically a single unit of a [[Riemann sum]] 

Now
$F(b)-F(a) = F(x_{n})-F(x_{0})$
This is just renaming the partition. One end of it is $x_n$ and the other is $x_0$
Rewriting this
$F(x_{n})-F(x_{0})$ = $F(x_{n})-F(x_{n-1})+F(x_{n-1})\dots -F(x_{1})+F(x_{1})-F(x_{0})$
This is because $-F(x_{n-1})+F(x_{n-1})$=0, so we aren't changing anything 

Rewriting this 
$(F(x_{n})-F(x_{n-1}))+(F(x_{n-1})-F(x_{n-2}))\dots+(F(x_{1})-F(x_{2}))$

Recall that 
$F(x_{i})-F(x_{i-1})=f(x_{i}^*)\Delta x$
thus 
$=f(x_{n}^*)\Delta x+f(x_{n-1}^*)\Delta x+\dots+f(x_{1}^*)\Delta x+$
In sigma notation ([[Riemann sum]])
$F(b)-F(a) = \sum_{i=1}^nf(x_{i}^*)\Delta x$

