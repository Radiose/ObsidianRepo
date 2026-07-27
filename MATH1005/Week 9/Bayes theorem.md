Bayes [[theorem]]
For any [[Probability experiment]] with a [[Sample space]] of $S$, for any $n \in \mathbb{N}$, for any [[partition]] $\{ B, \dots,B_{n} \}$ of S and any event $A \subset S$, if $\mathbb{P}(A) \not= 0$ and for all $i \in \{1,2\dots n \}$ we have $\mathbb{P}(B_{i}) \not= 0$, then for all $k \in \{ 1,2..n \}$, we have $\mathbb{P}(B_{k}|A)=\frac{\mathbb{P}(A|B_{K})\mathbb{P}(B_{K})}{\sum_{i=1}^n \mathbb{P}(A|B_{i})\mathbb{P}(B_{i})}$

So this is way to find the probability of B given A, when you only have the probability of A given B. 

K is the specific hypothesis you want to find. I is the running index. It loops through all hypothesises to build a denominator. 
The sum builds the total probability of A by considering every way A could happen.