---
aliases:
  - expected value
---
Random variable
A simple random variable on a subspace S is any function $X: S \to \mathbb{Q}$. It can be thought of as this outcome goes to this number. For simplicity, dying at 20 -> 1, dying at 40 -> 2...

We will denote the event "the random variable $X$ is equal to $a$" by $\{ X = a \}$, instead of the more formal, $\{s \in S| X(s) = a\}$

$P:S→\mathbb{Q}^+$  $X:S→\mathbb{Q}$

Random variables allow for non [[Equal likelihood models]]
Example: S = $\{ H,T \}^3$
$X(a,b,c)$ denotes the number of heads amongst a,b,c
$\{ X=2 \}=\{HHT  \},\{ HTH \},\{ THH \}$
We relate this to a probability [[Density function]]:

## Expectation
**The expected value**: $\mathbb{E}(x)=\sum_{s\in S}\mathbb{P}(s)X(s)$ = $\sum_{a \in Range(X)}\mathbb{P}(\{ X=a \})a$

In other words, the random variable maps an element in the sample space to an outcome. For example, this job maps to this life outcome.

The probability density function maps a probability to each random variable 

## Expectation of an indicator

An important identity is $\mathbb{E}[\mathbb{1}\{ A \}]=\mathbb{P}(A)+0\cdot(1-\mathbb{P}(A))=\mathbb{P}(A)$
For a random variable that is binary, the [[Random variable|expected value]] is also the probability. 
This is used constantly. The error of some classifier $h$ is $\mathbb{P}(h(\mathbf{X})\not=Y)=\mathbb{E}[\mathbb{1}(h(\mathbf{X})\not=Y)]$

### Linearity of expectation 
Note that random variables exhibit [[linearity]]
$\mathbb{E}[aX +bY]=a \mathbb{E}[X]+b\mathbb{E}[Y]$


### Multivariable expectation 
The [[Random variable|expected value]] of a function $g(X,Y)$ of two discrete, random variables is defined as $E(g(X,Y))=\sum_{x}\sum_{y}g(X,Y)p(X=x,Y=y)$

In particular, the expected value of $X$ is given by $E[X]=\sum_{x}\sum_{y}x\cdot p(X=x,Y=y)$


![[covariance]]



# In machine learning 
We treat discrete random variables as labels. It is particularly useful for [[supervised learning]].


# Continuous random variables

Often, we are dealing with quantities that are impossible to model discretely. For this reason, we use [[continuous function|continuous]] intervals properties. 

![[Density function#Continuous| continuous density function]]


The expectation of a [[continuous function|continuous]] random variable is defined is $\mathbb{E}[X]=\int_{-\infty}^\infty xf(x)dx$
