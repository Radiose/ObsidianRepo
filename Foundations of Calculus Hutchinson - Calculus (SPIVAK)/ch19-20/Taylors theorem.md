Taylors theorem 
Suppose that $f', \ldots, f^{(n+1)}$ are defined on $[a,x]$, and that $R_{n,a}(x)$ is defined by

$$f(x) = f(a) + f'(a)(x-a) + \cdots + \frac{f^{(n)}(a)}{n!}(x-a)^n + R_{n,a}(x).$$

Then

$$(1)\quad R_{n,a}(x) = \frac{f^{(n+1)}(t)}{n!}(x-t)^n(x-a) \quad \text{for some } t \text{ in } (a,x).$$

$$(2)\quad R_{n,a}(x) = \frac{f^{(n+1)}(t)}{(n+1)!}(x-a)^{n+1} \quad \text{for some } t \text{ in } (a,x).$$

Moreover, if $f^{(n+1)}$ is integrable on $[a,x]$, then

$$(3)\quad R_{n,a}(x) = \int_a^x \frac{f^{(n+1)}(t)}{n!}(x-t)^n\,dt.$$

(If $x < a$, then the hypothesis should state that $f$ is $(n+1)$-times differentiable on $[x,a]$; the number $t$ in (1) and (2) will then be in $(x,a)$, while (3) will remain true as stated, provided that $f^{(n+1)}$ is integrable on $[x,a]$.)


**PROOF** For each number $t$ in $[a,x]$ we have

$$f(x) = f(t) + f'(t)(x-t) + \cdots + \frac{f^{(n)}(t)}{n!}(x-t)^n + R_{n,t}(x).$$

Let us denote the number $R_{n,t}(x)$ by $S(t)$; since the function $S$ is defined on $[a,x]$, and

$$(*)\quad f(x) = f(t) + f'(t)(x-t) + \cdots + \frac{f^{(n)}(t)}{n!}(x-t)^n + S(t)$$

for all $t$ in $[a,x]$.

We will now differentiate both sides of this equation, taking with each equality the assertion of two functions: the one whose value at $t$ is $f(x)$, and the one whose value at $t$ is

$$f(t) + \cdots + \frac{f^{(n)}(t)}{n!}(x-t)^n + S(t).$$

(In common parlance we are considering both sides of $(*)$ "as a function of $t$." Just to make sure that the letter $x$ causes no confusion, notice that if

$$g(t) = f(x) \quad \text{for all } t,$$

then

$$g'(t) = 0 \quad \text{for all } t;$$

and if

$$g(t) = \frac{f^{(k)}(t)}{k!}(x-t)^k,$$

then

$$g'(t) = \frac{f^{(k+1)}(t)}{k!}(x-t)^k(-1) + \frac{f^{(k)}(t)}{k!}\cdot k(x-t)^{k-1}(-1)$$
$$= -\frac{f^{(k)}(t)}{(k-1)!}(x-t)^{k-1} + \frac{f^{(k+1)}(t)}{k!}(x-t)^k.$$

Applying these formulas to each term of $(*)$, we obtain

$$0 = f'(t) + \left[-f'(t) + \frac{f''(t)}{1!}(x-t)\right] + \left[-\frac{f''(t)}{1!}(x-t) + \frac{f'''(t)}{2!}(x-t)^2\right]$$
$$+ \cdots + \left[-\frac{f^{(n)}(t)}{(n-1)!}(x-t)^{n-1} + \frac{f^{(n+1)}(t)}{n!}(x-t)^n\right] + S'(t).$$

In the beautiful formula practically everything in sight cancels out, and we obtain

$$S'(t) = -\frac{f^{(n+1)}(t)}{n!}(x-t)^n.$$
### Cauchy
Now we can apply the Mean Value Theorem to the function $S$ on $[a,x]$: there is some $t$ in $(a,x)$ such that

$$\frac{S(x) - S(a)}{x-a} = S'(t) = -\frac{f^{(n+1)}(t)}{n!}(x-t)^n.$$

Remember that

$$S(t) = R_{n,t}(x);$$

this means in particular that

$$S(x) = R_{n,x}(x) = 0, \qquad S(a) = R_{n,a}(x).$$

Thus

$$\frac{0 - R_{n,a}(x)}{x-a} = -\frac{f^{(n+1)}(t)}{n!}(x-t)^n$$

or

$$R_{n,a}(x) = \frac{f^{(n+1)}(t)}{n!}(x-t)^n(x-a);$$

this is the Cauchy form of the remainder.


### Lagrange
To derive the Lagrange form we apply the Cauchy Mean Value Theorem for the functions $S$ and $g(t) = (x-t)^{n+1}$: there is some $t$ in $(a,x)$ such that

$$\frac{S(x)-S(a)}{g(x)-g(a)} = \frac{S'(t)}{g'(t)} = \frac{-\dfrac{f^{(n+1)}(t)}{n!}(x-t)^n}{-(n+1)(x-t)^n}.$$

Thus

$$\frac{R_{n,a}(x)}{(x-a)^{n+1}} = \frac{f^{(n+1)}(t)}{(n+1)!}$$

or

$$R_{n,a}(x) = \frac{f^{(n+1)}(t)}{(n+1)!}(x-a)^{n+1},$$

which is the Lagrange form.

Finally, if $f^{(n+1)}$ is integrable on $[a,x]$, then

$$S(x) - S(a) = \int_a^x S'(t)\,dt = -\int_a^x \frac{f^{(n+1)}(t)}{n!}(x-t)^n\,dt$$

or$$R_{n,a}(x) = \int_a^x \frac{f^{(n+1)}(t)}{n!}(x-t)^n\,dt. \blacksquare$$
