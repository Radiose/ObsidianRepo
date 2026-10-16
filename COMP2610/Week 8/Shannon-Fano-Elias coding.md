---
aliases:
  - SFE coding
  - SFE code
---
This is a form of coding designed to fix the problems outlined in [[Interval coding]] relating to the infinite recurring decimals requiring infinite numbers of bits to display correctly. 

The basic idea is to code, using the first $\ell(\mathbf{x})=\left\lceil  \log_{2} \frac{1}{p(\mathbf{x})}  \right\rceil+1$ bits of $\overline{F}(\mathbf{x})$


# Example 
![[Pasted image 20261016102608.png|397]]

![[Pasted image 20261016102621.png|454]]


This procedure is very simple, and has very significant properties. 

# Lossless property 

Recall the definition of lossless code(basically just injectivity)
We denote the Shannon-Fano-Elias code for an outcome $x$ by $\lfloor \bar{F}(x) \rfloor_{\ell(x)}$, (which means truncate to the first $\ell_{x}$ bits). 

Because $F(x-1)<\lfloor \bar{F}(x) \rfloor_{\ell(x))}<F(x)$, there is no possibility for overlap. This is because the code sits entirely in the interval between $x-1$ and $x$


# Prefix property 


## Background

Consider the set of binary strings that begin with $\mathbf{b}=b_{1},\dots,b_{n}$
Elements look like $b_{1}\dots b_{n}0,\ \ b_{1}\dots b_{n}1\dots$

Now consider the association $0.b_{1}\dots b_{n}$ as a prefix 

Note that $0.b_{1},\dots,b_{n}\bar{1}=0.b_{1},\dots,b_{n}+\frac{1}{2^n}=0.b_{1}\dots,b_{n}+0.0\dots {1}$
Similar to how $0.1\overline{9}_{10}=0.2$

Now, we start to use these things in relation to the interval. 
The set of numbers in $[0,1)$ that start with a given sequence $b_{1},\dots,b_{n}$ form the interval $$[0.b_{1},\dots,b_{n},0.b_{1},\dots b_{n}+\frac{1}{2^n})=[0.b_{1},\dots,b_{n},0.b_{1},\dots,b_{n}+0.0\dots {0}1) \\ \\(\text{with  } n-2\times {0} \text{  in the} \dots)$$

Examples include $1 \to [0.1,1.0)$ = $[0.5,1]_{10}$
$01 \to [0.01,0.10)=[0.25,1.0]_{10}$
$1101 \to [0.1101,0.1110)=[0.8125,0.1110]_{10}$

### Relating to prefixes

There are two forms of the "prefix property"
Tree form:
Once you pick a node in the binary [[tree]], you cannot pick any of its descendants. This was outlined in [[Kraft inequality]]

Interval form:
Once you pick a codeword $b_{1},\dots,b_{n}$, you cannot pick any codeword in $$[0.b_{1},\dots,b_{n},0.b_{1}b_{2},\dots,b_{n} +\frac{1}{2^n})$$
Intuitively, this contains all binary strings for which $b_{1},\dots,b_{n}$ is a prefix, so similar to the binary tree idea, its not here. 


If $\mathbf{b}'$ is a prefix of $\mathbf{b}$, the interval of $\mathbf{b}$ is contained in the interval for $\mathbf{b}'$
For example, $\mathbf{b}'=01$ is a prefix of $\mathbf{b}=0101$, so $[0.0101,0.0110) \subset [0.01,0.10)$

This is because the interval for $\mathbf{b}'$ contains all the strings, for which $\mathbf{b}'$ is a prefix.
And if $\mathbf{b}$ has $\mathbf{b}'$ as a prefix, so does anything having $\mathbf{b}$ as a prefix. 

This has a significant implication, being that if intervals of $\mathbf{b},\mathbf{b}'$ are disjoint, then one **cannot** be a prefix of another. 

## Why SFE is prefix free 
We know that $\lfloor \bar{F}(x) \rfloor_{\ell(x)}<\bar{F}(x)$, so
$$\begin{aligned}
\lfloor \overline{F}(x) \rfloor_{\ell(x)} + \frac{1}{2^{\ell}} &\le \overline{F}(x) + \frac{1}{2^{\ell}} \\
&\le \overline{F}(x) + \frac{p(x)}{2} \\
&= F(x),
\end{aligned}$$

# Symbol interval
The symbol interval for some outcome $x_{i}$ is (assuming $F(x_{0})=0$) $$[F(x_{i-1}),F(x_{i}))$$
# Codeword interval 
For some outcome $x_{i}$ is $$\left[ \lfloor \bar{F}(x_{i}) \rfloor_{\ell(x_{i})},\lfloor \bar{F}(x_{i}) \rfloor_{\ell(x_{i})}+\frac{1}{2^{\ell(x_{i})}}   \right]$$This is a strict subset of the symbol interval.
Note that all strings in the codeword interval start with the same prefix, but this is **not** true for the symbol interval.


# The [[expected code length]]
There can be an extra bit for these code lengths, because we code $\frac{p_{i}}{2}$ (the midpoint)
and then $\log_{2} \frac{2}{p_{i}}=\log_{2} \frac{1}{p_{i}}+1$

Thus, $L(C,X)=\sum_{i=1}^K p_{i}\ell(a_{i})= \sum_{i=1}^K p_{i}\left( \left\lceil  \log_{2} \frac{1}{p_{i}}  \right\rceil+1 \right)$
$$\leq \sum_{i=1}^K p_{i}\left( \log_{2} \frac{1}{p_{i}}+2 \right)\\H(X)+2$$
So we have lower bound $H(X)+1\leq L(C,X)$ as a lower bound. 