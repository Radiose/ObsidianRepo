---
aliases:
  - Taylor series
  - Taylor approximation
---
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

The trick was to take the $n-1$ derivative via [[L'Hopital's rule]] and then notice that that is nothing but a derivative. 


A consequence of this theorem is that we can perfect the test for [[Maxima and minima|maxima or minima]] over an interval. 

# Theorem 2
Suppose that

$$f'(a) = \cdots = f^{(n-1)}(a) = 0,$$
$$f^{(n)}(a) \ne 0.$$

(1) If $n$ is even and $f^{(n)}(a) > 0$, then $f$ has a local minimum at $a$.
(2) If $n$ is even and $f^{(n)}(a) < 0$, then $f$ has a local maximum at $a$.
(3) If $n$ is odd, then $f$ has neither a local maximum nor a local minimum at $a$.

**PROOF** There is clearly no loss of generality in assuming that $f(a) = 0$, since neither the hypotheses nor the conclusion are affected if $f$ is replaced by $f - f(a)$. Then, since the first $n-1$ derivatives of $f$ at $a$ are $0$, the Taylor polynomial $P_{n,a}$ of $f$ is

$$P_{n,a}(x) = f(a) + \frac{f'(a)}{1!}(x-a) + \cdots + \frac{f^{(n)}(a)}{n!}(x-a)^n$$
$$= \frac{f^{(n)}(a)}{n!}(x-a)^n.$$

Thus, Theorem 1 states that

$$0 = \lim_{x\to a} \frac{f(x) - P_{n,a}(x)}{(x-a)^n} = \lim_{x\to a}\left[\frac{f(x)}{(x-a)^n} - \frac{f^{(n)}(a)}{n!}\right].$$

Consequently, if $x$ is sufficiently close to $a$, then

$$\frac{f(x)}{(x-a)^n} \text{ has the same sign as } \frac{f^{(n)}(a)}{n!}.$$

Suppose now that $n$ is even. **In this case $(x-a)^n > 0$** for all $x \ne a$. Since $f(x)/(x-a)^n$ has the same sign as $f^{(n)}(a)/n!$ for $x$ sufficiently close to $a$, it follows that $f(x)$ itself has the same sign as $f^{(n)}(a)/n!$ for $x$ sufficiently close to $a$. If $f^{(n)}(a) > 0$, this means that

$$f(x) > 0 = f(a)$$

for $x$ close to $a$. Consequently, $f$ has a local minimum at $a$. A similar proof works for the case $f^{(n)}(a) < 0$.

Now suppose that $n$ is odd. The same argument as before shows that if $x$ is sufficiently close to $a$, then

$$\frac{f(x)}{(x-a)^n} \text{ always has the same sign.}$$

But $(x-a)^n > 0$ for $x > a$ and $(x-a)^n < 0$ for $x < a$. Therefore $f(x)$ has *different* signs for $x > a$ and $x < a$. This proves that $f$ has neither a local maximum nor a local minimum at $a$. $\blacksquare$

The trick was to use $f(a)=0$ to simplify the Taylor polynomial to a singular term that we can then make theorem 1 ultra easy to use. The other important thing to notice was that we can tell the sign based off the fact that 


### Equal up to order n 
If 
$$\lim_{ x \to a } \frac{f(x)-g(x)}{(x-a)^n} =0$$
then we say that $f$ and $g$ are **equal up to order n**
The Taylor polynomial, via theorem 1 states that $P_{n,a,f}$ equals $f$ up to order $n$. The Taylor polynomial is unique, as its the only one that satisfies this. This is highlighted in the next theorem. 


# Theorem 3

Let $P$ and $Q$ be two polynomials in $(x-a)$, of degree $\le n$, and suppose that $P$ and $Q$ are equal up to order $n$ at $a$. Then $P = Q$.

**PROOF** Let $R = P - Q$. Since $R$ is a polynomial of degree $\le n$, it is only necessary to prove that if

$$R(x) = b_0 + \cdots + b_n(x-a)^n$$

satisfies

$$\lim_{x\to a} \frac{R(x)}{(x-a)^n} = 0,$$

then $R = 0$. Now the hypotheses on $R$ surely imply that

$$\lim_{x\to a} \frac{R(x)}{(x-a)^i} = 0 \quad \text{for } 0 \le i \le n.$$

For $i=0$ this condition reads simply $\lim_{x\to a} R(x) = 0$; on the other hand,

$$\lim_{x\to a} R(x) = \lim_{x\to a}\left[b_0 + b_1(x-a) + \cdots + b_n(x-a)^n\right]$$
$$= b_0.$$

Thus $b_0 = 0$ and

$$R(x) = b_1(x-a) + \cdots + b_n(x-a)^n.$$

Therefore,

$$\frac{R(x)}{x-a} = b_1 + b_2(x-a) + \cdots + b_n(x-a)^{n-1}$$

and

$$\lim_{x\to a} \frac{R(x)}{x-a} = b_1.$$

Thus $b_1 = 0$ and

$$R(x) = b_2(x-a)^2 + \cdots + b_n(x-a)^n.$$

Continuing in this way, we find that

$$b_0 = \cdots = b_n = 0. \blacksquare$$
This is basically just [[Induction]]. The trick here was to create a polynomial $R$.


# COROLLARY

Let $f$ be $n$-times differentiable at $a$, and suppose that $P$ is a polynomial in $(x-a)$ of degree $\le n$, which equals $f$ up to order $n$ at $a$. Then $P = P_{n,a,f}$.

**PROOF** Since $P$ and $P_{n,a,f}$ both equal $f$ up to order $n$ at $a$, it is easy to see that $P$ equals $P_{n,a,f}$ up to order $n$ at $a$. Consequently, $P = P_{n,a,f}$ by the Theorem. $\blacksquare$

At first sight this corollary appears to have unnecessarily complicated hypotheses; it might seem that the existence of the polynomial $P$ would automatically imply that $f$ is sufficiently differentiable for $P_{n,a,f}$ to exist. But in fact this is not so. For example, suppose that

$$f(x) = \begin{cases} x^{n+1}, & x \text{ irrational} \\ 0, & x \text{ rational}. \end{cases}$$

If $P(x) = 0$, then $P$ is certainly a polynomial of degree $\le n$ which equals $f$ up to order $n$ at $0$. On the other hand, $f'(a)$ does not exist for any $a \ne 0$, so $f''(0)$ is undefined.

![[Pasted image 20260729184553.png]]


# Approximating arctan


When $f$ does have $n$ derivatives at $a$, however, the corollary may provide a useful method for finding the Taylor polynomial of $f$. In particular, remember that our first attempt to find the Taylor polynomial for arctan ended in failure. The equation

$$\arctan x = \int_0^x \frac{1}{1+t^2}\,dt$$

suggests a promising method of finding a polynomial close to arctan—divide $1$ by $1+t^2$, to obtain a polynomial plus a remainder:

$$\frac{1}{1+t^2} = 1 - t^2 + t^4 - t^6 + \cdots + (-1)^n t^{2n} + \frac{(-1)^{n+1}t^{2n+2}}{1+t^2}.$$

This formula, which can be checked easily by multiplying both sides by $1+t^2$, shows that

$$\arctan x = \int_0^x 1 - t^2 + t^4 - \cdots + (-1)^n t^{2n}\, dt + (-1)^{n+1}\int_0^x \frac{t^{2n+2}}{1+t^2}\,dt$$
$$= x - \frac{x^3}{3} + \frac{x^5}{5} - \cdots + (-1)^n\frac{x^{2n+1}}{2n+1} + (-1)^{n+1}\int_0^x \frac{t^{2n+2}}{1+t^2}\,dt.$$
$$\arctan x = \underbrace{x - \frac{x^3}{3} + \frac{x^5}{5} - \cdots + (-1)^n\frac{x^{2n+1}}{2n+1}}_{P(x),\ \text{a polynomial}} ;+; \underbrace{(-1)^{n+1}\int_0^x \frac{t^{2n+2}}{1+t^2},dt}_{\text{call this } E(x)}.$$


According to our corollary, the polynomial which appears here will be the Taylor polynomial of degree $2n+1$ for arctan at $0$, provided that

$$\lim_{x\to 0} \frac{\displaystyle\int_0^x \frac{t^{2n+2}}{1+t^2}\,dt}{x^{2n+1}} = 0.$$
or that $E(x)$ will = 0 as $x \to 0$. (because the corollary states they are equal up to order n)
Since

$$\left|\int_0^x \frac{t^{2n+2}}{1+t^2}\,dt\right| \le \left|\int_0^x t^{2n+2}\,dt\right| = \frac{|x|^{2n+3}}{2n+3},$$

this is clearly true. Thus we have found that the Taylor polynomial of degree $2n+1$ for arctan at $0$ is

$$P_{2n+1,0}(x) = x - \frac{x^3}{3} + \frac{x^5}{5} - \cdots + (-1)^n\frac{x^{2n+1}}{2n+1}.$$


![[Remainder term]]

We have multiple ways of denoting the remainder term. One of which is to express it in terms of the integral, as we have done above with $\arctan$.

 ![[Taylors theorem]]