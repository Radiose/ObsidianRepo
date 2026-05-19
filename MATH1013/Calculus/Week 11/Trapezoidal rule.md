Trapezoidal rule

A slightly more accurate version than the [[Midpoint rule]], that utilised trapezoids instead of rectangles.
Note that the area of a trapezoid is given by 
$\frac{f(x_{i})+f(x_{i+1})}{2}\Delta x$
And the total sum of all trapezoids is given by 
$Tn​=\frac{Δx}{2}​[(f(x_{0}​)+f(x_{1}))+(f(x_{1}​)+f(x_{2}))+(f(x_{2}​)+f(x_{3}​))+⋯+(f(x_{n−1}​)+f(x_{n}​))]$ 
or more naturally 
$Tn = \frac{∆x}{2} [f (x_{0}) + 2f (x_{1}) + 2f (x_{2}) + · · · + 2f (x_{n−1}) + f (x_{n})$

### Error binding 
We bind the error via $\exists K \in \mathbb{R} \forall x \in [a,b] |f''(x)| \le K \implies E_{T}\le \frac{K(b-a)^3}{12n^2}$
