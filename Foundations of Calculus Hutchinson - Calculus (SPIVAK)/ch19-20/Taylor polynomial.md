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

Upon closer inspection, the Taylor polynomial of degree 1




![[Linear approximation]]