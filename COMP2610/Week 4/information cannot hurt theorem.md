For any two random variables $X,Y$,

$H(X|Y)\leq H(X)$,

with equality if and only if $X$ and $Y$ are independent.

### Proof
We simply use the non-negativity of mutual information:

$I(X;Y)\geq0$

$H(X)-H(X|Y)\geq0$

$H(X|Y)\leq H(X)$

with equality if and only if $p(X,Y)=p(X)p(Y)$, i.e. $X$ and $Y$ are independent.