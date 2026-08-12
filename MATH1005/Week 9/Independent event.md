---
aliases:
  - dependent event
  - independent
  - dependent
---
For a [[Sample space]] S with probability [[Density function]] P. $E,F \in \mathcal{P}(S)$ are called *independent* events when $\mathbb{P}(E \cap F)=\mathbb{P}(E)\times \mathbb{P}(F)$
Two random variables are independent when 
$\forall a \in Range(X)\ \ \forall b \in Range(Y)$
$\{ X=a \},\{ Y=b \}$ are independent

We also denote two independent events $x \mathrel{\perp\!\!\!\perp}y$ 


### Example 
Toss two coins: $(H+T)^2=\{ \{HT\}, \{TH\}, \{TT\}, \{ HH \}\}$
First toss is heads: $\mathbb{P}(G)=\frac{1}{4}+\frac{1}{4}=\frac{1}{2}$
Second toss is tails: $\mathbb{P}(A)=\frac{1}{4}+\frac{1}{4}=\frac{1}{2}$
First toss is heads and second toss is tails: $\frac{1}{4}$
$\mathbb{P}(G)\times P(A)=\frac{1}{4}$
Thus, the first toss being heads is an independent even from the second toss being tails.


The only way to prove that two [[random variable]]s are independent is to prove all entries are independent of each other. For example, to prove that height and grades are independent, you'd have to verify that the joint distribution factors at every point — $P(X=x \cap Y=y)=P(X=x)P(Y=y)$for all pairs $(x,y)$
