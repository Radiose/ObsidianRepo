---
aliases:
  - chain rule (mutual information)
---
This occurs when we want to find the [[mutual information]] between some $I(X;Y,Z)$, so between some [[random variable]] $X$ and the joint distribution between $Y,Z$. 
Note that $I(X,Y;Z)\not=I(X;Y,Z)$.

In order to calculate, we have to use the **chain rule.** 


# Derivation 
Let $X,Y,Z$ be r.v. and recall that:

$p(Z,Y)=p(Z|Y)p(Y)$

$H(Z,Y)=H(Z|Y)+H(Y)$

$I(X;Y,Z)=I(Y,Z;X)$ - by symmetry

$=H(Z,Y)-H(Z,Y|X)$

$=H(Z|Y)+H(Y)-H(Z|X,Y)-H(Y|X)$ - [[joint entropy|the chain rule(entropy)]]

$=H(Y)-H(Y|X)+H(Z|Y)-H(Z|X,Y)$

$=I(Y;X)+I(Z;X|Y)$ 

Therefore:

$I(X;Y,Z)=I(X;Y)+I(X;Z|Y)$

Similarly, by symmetry:

$I(X;Y,Z)=I(X;Z)+I(X;Y|Z)$

# General form

For any collection of random variables $X_1,\ldots,X_N$ and $Y$:

$I(X_1,\ldots,X_N;Y)=I(X_1;Y)+I(X_2,\ldots,X_N;Y|X_1)$

$=I(X_1;Y)+I(X_2;Y|X_1)+I(X_3,\ldots,X_N;Y|X_1,X_2)$

$=\ldots$

$=\sum_{i=1}^{N}I(X_i;Y|X_1,\ldots,X_{i-1})$

$=\sum_{i=1}^{N}I(Y;X_i|X_1,\ldots,X_{i-1})$

