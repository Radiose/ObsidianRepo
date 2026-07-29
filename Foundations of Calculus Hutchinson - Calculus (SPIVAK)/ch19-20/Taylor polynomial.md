# Derivation 
We will discover how to approximate several [[function]]s such as $\sin$, $\cos$, $\ln$ and more using polynomials. In order to do this, we first need to examine polynomials a bit closer. 
Suppose that $p(x)=a_{0}+a_{1}x+\dots+a_{n}x^n$. 
One very useful feature of polynomials, is that using the [[derivative]], we can any express coefficients $a_n$. 
Observe, $$p'(x) = a_1 + 2a_2x + \cdots + na_nx^{n-1}$$thus, $p'(0)=p^{1}(x)=a_{1}$

Differentiating again we obtain

$$p''(x) = 2a_2 + 3\cdot 2 \cdot a_3x + \cdots + n(n-1)\cdot a_nx^{n-2}.$$

Therefore,

$$p''(0) = p^{(2)}(0) = 2a_2.$$

In general, we will have

$$p^{(k)}(0) = k!\,a_k \quad \text{or} \quad a_k = \frac{p^{(k)}(0)}{k!}.$$
If we had begun with a function $p$ that was written as a "polynomial in $(x-a)$,"

$$p(x) = a_0 + a_1(x-a) + \cdots + a_n(x-a)^n,$$

then a similar argument would show that

$$a_k = \frac{p^{(k)}(a)}{k!}.$$

Suppose now that $f$ is a function (not necessarily a polynomial) such that

$$f^{(1)}(a), \ldots, f^{(n)}(a)$$

all exist. Let

$$a_k = \frac{f^{(k)}(a)}{k!}, \quad 0 \le k \le n,$$

and define

$$P_{n,a}(x) = a_0 + a_1(x-a) + \cdots + a_n(x-a)^n.$$
This polynomial is denoted the *Taylor polynomial* of degree $n$ for $f$ at $a$

## Taylor polynomials of sin, cos, exp
Although the coefficients of $P_{n,a,f}$ seem to depend upon $f$ in a fairly complicated way, the most important elementary functions have extremely simple Taylor polynomials. Consider first the function $\sin$. We have

$$\sin(0) = 0,$$
$$\sin'(0) = \cos 0 = 1,$$
$$\sin''(0) = -\sin 0 = 0,$$
$$\sin'''(0) = -\cos 0 = -1,$$
$$\sin^{(4)}(0) = \sin 0 = 0.$$

From this point on, the derivatives repeat in a cycle of 4. The numbers

$$a_k = \frac{\sin^{(k)}(0)}{k!}$$

are

$$0,\ 1,\ 0,\ -\frac{1}{3!},\ 0,\ \frac{1}{5!},\ 0,\ -\frac{1}{7!},\ 0,\ \frac{1}{9!},\ \ldots.$$

Therefore the Taylor polynomial $P_{2n+1,0}$ of degree $2n+1$ for $\sin$ at $0$ is

$$P_{2n+1,0}(x) = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots + (-1)^n\frac{x^{2n+1}}{(2n+1)!}.$$

(Of course, $P_{2n+1,0} = P_{2n+2,0}$.)

The Taylor polynomial $P_{2n,0}$ of degree $2n$ for $\cos$ at $0$ is (the computations are left to you)

$$P_{2n,0}(x) = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots + (-1)^n\frac{x^{2n}}{(2n)!}.$$

The Taylor polynomial for $\exp$ is especially easy to compute. Since $\exp^{(k)}(0) = \exp(0) = 1$ for all $k$, the Taylor polynomial of degree $n$ at $0$ is

$$P_{n,0}(x) = 1 + \frac{x}{1!} + \frac{x^2}{2!} + \frac{x^3}{3!} + \frac{x^4}{4!} + \cdots + \frac{x^n}{n!}.$$


# Relating to linear approximation 

Upon closer inspection, the Taylor polynomial of degree 1 is exactly that of the one used in [[Linear approximation]]. 


$$P_{1,a}(x) = f(a) + f'(a)(x-a).$$

Notice that

$$\frac{f(x) - P_{1,a}(x)}{x-a} = \frac{f(x)-f(a)}{x-a} - f'(a).$$

Now, by the definition of $f'(a)$ we have

$$\lim_{x\to a} \frac{f(x) - P_{1,a}(x)}{x-a} = 0.$$

Viewing the image below, we can see some patterns

![[Pasted image 20260729160425.png]]

We see the difference between $P_{2,0}$ seems to be less than that of $P_{1,0}$


Thus, we derive some expression for second degree [[Taylor polynomial]]s, and notice if $f'(a)$ and $f''(a)$ exist, then

$$\lim_{x\to a} \frac{f(x) - P_{2,a}(x)}{(x-a)^2} = 0;$$

in fact, the analogous assertion for $P_{n,a}$ is also true. We show it in *theorem 1*

# Theorem 1


Suppose that $f$ is a function for which

$$f'(a), \ldots, f^{(n)}(a)$$

all exist. Let

$$a_k = \frac{f^{(k)}(a)}{k!}, \quad 0 \le k \le n,$$

and define

$$P_{n,a}(x) = a_0 + a_1(x-a) + \cdots + a_n(x-a)^n.$$

Then

$$\lim_{x\to a} \frac{f(x) - P_{n,a}(x)}{(x-a)^n} = 0.$$



**PROOF** Writing out $P_{n,a}(x)$ explicitly, we obtain

$$\frac{f(x) - P_{n,a}(x)}{(x-a)^n} = \frac{f(x) - \displaystyle\sum_{i=0}^{n-1}\frac{f^{(i)}(a)}{i!}(x-a)^i}{(x-a)^n} - \frac{f^{(n)}(a)}{n!}.$$

It will help to introduce the new functions

$$Q(x) = \sum_{i=0}^{n-1}\frac{f^{(i)}(a)}{i!}(x-a)^i \quad \text{and} \quad g(x) = (x-a)^n;$$

now we must prove that

$$\lim_{x\to a}\frac{f(x)-Q(x)}{g(x)} = \frac{f^{(n)}(a)}{n!}.$$

Notice that

$$Q^{(k)}(a) = f^{(k)}(a), \quad k \le n-1,$$
$$g^{(k)}(x) = n!(x-a)^{n-k}/(n-k)!.$$
(test it out)
Thus

$$\lim_{x\to a}[f(x) - Q(x)] = f(a) - Q(a) = 0,$$
$$\lim_{x\to a}[f'(x) - Q'(x)] = f'(a) - Q'(a) = 0,$$
$$\vdots$$
$$\lim_{x\to a}[f^{(n-2)}(x) - Q^{(n-2)}(x)] = f^{(n-2)}(a) - Q^{(n-2)}(a) = 0.$$

and

$$\lim_{x\to a} g(x) = \lim_{x\to a} g'(x) = \cdots = \lim_{x\to a} g^{(n-2)}(x) = 0.$$

We may therefore apply l'Hôpital's Rule $n-1$ times to obtain

$$\lim_{x\to a}\frac{f(x)-Q(x)}{(x-a)^n} = \lim_{x\to a}\frac{f^{(n-1)}(x) - Q^{(n-1)}(x)}{n!\,(x-a)}.$$

Since $Q$ is a polynomial of degree $n-1$, its $(n-1)$st derivative is a constant; in fact, $Q^{(n-1)}(x) = f^{(n-1)}(a)$. Thus

$$\lim_{x\to a}\frac{f(x)-Q(x)}{(x-a)^n} = \lim_{x\to a}\frac{f^{(n-1)}(x) - f^{(n-1)}(a)}{n!\,(x-a)}$$
(note this is just a [[derivative]])
and this last limit is $f^{(n)}(a)/n!$ by definition of $f^{(n)}(a)$. $\blacksquare$


A consequence of this theorem 



![[Linear approximation]]