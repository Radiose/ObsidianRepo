# Definition

if $$X \to Y \to Z$$([[markov chain]]), then $$I(X;Y)\geq I(X;Z)$$
X is the state of the world, $Y$ is the data gathered, $Z$ is the processed data.


# Proof
Recall that the [[joint mutual information|chain rule (mutual information)]] states that:

$I(X;Y,Z)=I(X;Y)+I(X;Z|Y)$

$=I(X;Z)+I(X;Y|Z)$

Therefore:

$I(X;Y)+I(X;Z|Y)=I(X;Z)+I(X;Y|Z)$

$$ \underbrace{I(X;Z|Y)}_{0} $$

$\quad I(X;Y)=I(X;Z)+I(X;Y|Z)$
$$ \qquad\qquad\qquad\qquad\text{but }I(X;Y|Z)\geq0$$

$I(X;Y)\geq I(X;Z)$



# Corollary 1
If $Z=g(Y)$, then $I(X;Y)\geq I(X,g(Y))$

The proof is that $X \to Y \to g(Y)$ forms a [[markov chain]]

Basically, functions of data $Y$ cannot increase the information about $X$

# Corollary 2 

If $X\to Y \to Z$, then $I(X;Y|Z)\leq I(X;Y)$

The dependence on $X$ and $Y$ cannot be increased by the observation of a downstream variable. 


### Proof:
We use the [[joint mutual information|chain rule (mutual information)]]:

$I(X;Y,Z)=I(X;Y)+I(X;Z|Y)$

$=I(X;Z)+I(X;Y|Z)$

Therefore:

$I(X;Y)+\underbrace{I(X;Z|Y)}_{0}=I(X;Z)+I(X;Y|Z)$
 

$I(X;Y|Z)=I(X;Y)-I(X;Z)$

$\qquad\qquad\qquad\text{but }I(X;Z)\geq0$

$I(X;Y|Z)\leq I(X;Y)$


