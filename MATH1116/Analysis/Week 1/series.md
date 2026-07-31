A series is a type of [[Sequence]] that is defined in terms of addition. 





some notes:
To add series, directly, they must have the same index range. 
$\sum_{i=0}^n a_{n} + \sum_{i=0}^n b_{n} = \sum_{i=0}^n(a_{n}+b_{n})$

# Reindexing series (and peeling)
This is an essential skill for adding series that have differing ranges.
### A simple example 


Two misaligned sums are shown below

$$\sum_{i=0}^{2} x^{i+1} \qquad\text{and}\qquad \sum_{i=0}^{2} x^{i}$$

Written out: first is $x^1+x^2+x^3$, second is $x^0+x^1+x^2$.

We reindex the first sum so its exponent matches the second's variable name. Let $j = i+1$ (so $i=j-1$). Limits shift too: $i=0\to j=1$, $i=2\to j=3$.

$$\sum_{i=0}^{2}x^{i+1} = \sum_{j=1}^{3}x^{j}$$


We then notice ranges aren't matching up. The first sum is $j=1$ to $3$, second is $j=0$ to $2$. Peel off the non-overlapping ends:

- From sum 1, peel $j=3$: leaves $\sum_{j=1}^{2}x^j$, plus leftover $x^3$
- From sum 2, peel $j=0$: leaves $\sum_{j=1}^{2}x^j$, plus leftover $x^0$

Now we can add these all together

$$\sum_{j=1}^{2}x^j + \sum_{j=1}^{2}x^j = \sum_{j=1}^{2}2x^j$$

$$\text{Total} = x^0 + \sum_{j=1}^{2}2x^j + x^3 = 1 + 2x + 2x^2 + x^3$$
It may be confusing to think about why we don't need to substitute $i$ back in. Think about what $i$ actually represents, *does it ever have an actual value?*


### A complex example:

Say you wanted to add
$$\sum_{i=0}^n\binom{n}{i}x^{i+1}y^{n-i} \qquad \text{and} \qquad \sum_{i=0}^n\binom{n}{i}x^{i}y^{n-i+1}$$
in the monomial, we have differing powers, so we need to reindex them to add them properly. 
We notice that by creating some $j = i+1$ for the first sum, and $j=i$ for the second sum, we can make monomial powers match up  


$$\sum_{i=0}^n\binom{n}{i}x^{i+1}y^{n-i} ;\longrightarrow;\ \ \ \ \  \sum_{j=1}^{n+1}\binom{n}{j-1}x^{j}y^{n-j+1} + \sum_{j=0}^n\binom{n}{j}x^{j}y^{n-j+1}$$

Now both sums are written as coefficient $\times, x^jy^{n+1-j}$ we are ready to combine.

We run into the main problem though, that being that our index ranges are not correctly ranged to add. We need to peel off $j=0$ for the right hand sum, and $j=n+1$ for the left hand sum. 

Peeled from the $j = 1$ to $n+1$ sum (the $j = n+1$ term):

$$\binom{n}{n}x^{n+1}y^{0} = x^{n+1}$$

Peeled from the $j = 0$ to $n$ sum (the $j = 0$ term):

$$\binom{n}{0}x^{0}y^{n+1} = y^{n+1}$$

Final assembled expression:
$$= x^{n+1} + y^{n+1} + \sum_{j=1}^{n}\left[\binom{n}{j-1}+\binom{n}{j}\right]x^{j}y^{n+1-j}$$
(via pascals rule)
$$= x^{n+1} + y^{n+1} + \sum_{j=1}^{n}\binom{n+1}{j}x^{j}y^{n+1-j}$$

$$= \sum_{j=0}^{n+1}\binom{n+1}{j}x^{j}y^{n+1-j}$$


# Convergence of series
Series, like [[Sequence]]s can [[Convergence of a sequence|converge]]. 