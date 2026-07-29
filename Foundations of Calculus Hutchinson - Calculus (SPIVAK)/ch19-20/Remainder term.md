Remainder term
An interesting fact occurs when we go back to the equation where we [[Taylor polynomial#Approximating arctan|approximated arctan]]

$$\arctan x = x - \frac{x^3}{3} + \frac{x^5}{5} - \cdots + (-1)^n\frac{x^{2n+1}}{2n+1} + (-1)^{n+1}\int_0^x \frac{t^{2n+2}}{1+t^2}\,dt,$$

and remember the estimate

$$\left|\int_0^x \frac{t^{2n+2}}{1+t^2}\,dt\right| \le \frac{|x|^{2n+3}}{2n+3}.$$
When $|x|\leq 1$, this equation is at most $\frac{1}{2n+3}$ and we can make this as small as we want. Thus, we can make $\arctan x$ as accurate as we want for $|x|\leq 1$.


We now begin to define [[Taylor polynomial]]s $P_{n,a}$ for a *fixed $x$*, and different $n$, while previously we defined them in terms of fixed $n$ as $x$ approaches $a$.

If $f$ is a function for which $P_{n,a}(x)$ exists, we define the **remainder term** $R_{n,a}(x)$ by

$$f(x) = P_{n,a}(x) + R_{n,a}(x)$$
$$= f(a) + f'(a)(x-a) + \cdots + \frac{f^{(n)}(a)}{n!}(x-a)^n + R_{n,a}(x).$$

