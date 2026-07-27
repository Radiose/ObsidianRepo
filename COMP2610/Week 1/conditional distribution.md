conditional distribution 

This is a form of [[Cumulative probability distribution function|distribution function]] that applies to [[Conditional probability]].
To be precise, its defined by $p(X=x|Y=y)=\frac{p(X=x \cap Y=y)}{p(Y=y)}$, where the sum of all $X$ given $y$ should equal 1. 
To simplify, if we have some fixed $y$, and two possible $x$ for $X$, then $p(X =x_{1}|Y=y) +P(X=x_{2}|Y=y)=1$.

![[Pasted image 20260727133903.png]]
EG:

#### 1. For $Y = -1$:

- $P(X = 0 \mid Y = -1) = \frac{P(X=0, Y=-1)}{P(Y=-1)} = \frac{0}{1/3} = 0$
    
- $P(X = 1 \mid Y = -1) = \frac{P(X=1, Y=-1)}{P(Y=-1)} = \frac{1/3}{1/3} = 1$
    

 **Distribution for $Y = -1$:** $p(X=0 \mid Y=-1) = 0$, $p(X=1 \mid Y=-1) = 1$

#### 2. For $Y = 0$:

- $P(X = 0 \mid Y = 0) = \frac{P(X=0, Y=0)}{P(Y=0)} = \frac{1/3}{1/3} = 1$
    
- $P(X = 1 \mid Y = 0) = \frac{P(X=1, Y=0)}{P(Y=0)} = \frac{0}{1/3} = 0$
    

 **Distribution for $Y = 0$:** $p(X=0 \mid Y=0) = 1$, $p(X=1 \mid Y=0) = 0$

#### 3. For $Y = 1$:

- $P(X = 0 \mid Y = 1) = \frac{P(X=0, Y=1)}{P(Y=1)} = \frac{0}{1/3} = 0$
    
- $P(X = 1 \mid Y = 1) = \frac{P(X=1, Y=1)}{P(Y=1)} = \frac{1/3}{1/3} = 1$
    
**Distribution for $Y = 1$:** $p(X=0 \mid Y=1) = 0$, $p(X=1 \mid Y=1) = 1$