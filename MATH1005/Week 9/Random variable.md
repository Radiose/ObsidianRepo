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

**The expected value**: $\mathbb{E}(x)=\sum_{s\in S}\mathbb{P}(s)X(s)$ = $\sum_{a \in Range(X)}\mathbb{P}(\{ X=a \})a$

In other words, the random variable maps an element in the sample space to an outcome. For example, this job maps to this life outcome.

The probability density function maps a probability to each random variable 

