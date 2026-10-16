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

Consider the set of binary strings that begin with $\mathbf{b}=b_{1},\dots,b_{n}$
Elements look like $b_{1}\dots b_{n}0,\ \ b_{1}\dots b_{n}1\dots$

Now consider the association $0.b_{1}\dots b_{n}$ as a prefix 

Note that $0.b_{1},\dots,b_{n}\bar{1}=0.b_{1},\dots,b_{n}+\frac{1}{2^n}=0.b_{1}\dots,b_{n}+0.0\dots {1}$
Similar to how $0.1\overline{9}_{10}=0.2$

Now, we start to use these things in relation to the interval. 