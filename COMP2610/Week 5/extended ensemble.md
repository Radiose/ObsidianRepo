Note that we consider blocks of outcomes as a method to describe [[sequence]]s.

![[Pasted image 20260826172741.png]]



Let $X$ be a single [[ensemble]]. The [[extended ensemble]] of blocks of size $N$ is denoted $X^N$. Outcomes from $X^N$ are denoted $\mathbf{x}=(x_{1},x_{2},\dots,x_{N})$
The probability of $\mathbf{x}$ is denoted to be $P(\mathbf{x})=P(x_{1})P(x_{2})\dots P(x_{N})$


# Example 

Let $X$ be an ensemble with outcomes $\mathcal{A}_X = \{\text{h}, \text{t}\}$ with $p_h = 0.9$ and $p_t = 0.1$.

Consider $X^4$ — i.e., 4 flips of the coin.
$$\mathcal{A}_{X^4} = \{\text{hhhh}, \text{hhht}, \text{hhth}, \ldots, \text{tttt}\}$$
Suppose the probability of a head is 0.9, and the probability of tails is 0.1
$P(hhhh)=(0.9)^4$
$P(tttt)=(0.1)^4$



![[Entropy of extended ensembles]]



# The probability of an ensemble 

Let $X$ be an [[ensemble]] with an alphabet $A_{X}$.
let $p(X=a_{i})=p_{i}$
For a sequence $\mathbf{x}=x_{1},x_{2},\dots,x_{n}$, how to calculate $p(\mathbf{x})$?

let $n_{i}$ be the number of time the symbol $a_{i}$ appears in $\mathbf{x}$.
For each value in the alphabet, we get the probability of that value and multiply it by the amount of times it occurs. 
So, $P(\mathbf{x})=P(x_{1})P(x_{2})\dots P(x_{n})$
$=P(a_{1})^{n_{1}}\cdot P(a_{2})^{n_{2}}\dots \cdot P(a_{i})^{n_{i}}$
$=p_{1}^{n_{1}}\cdot p_{2}^{n_{2}}\dots p_{I}^{n_{I}}$
we use [[the multinomial coefficient]]  to calculate then the number of ways an [[ensemble]] can look. 


![[the multinomial coefficient]]


# Example 
Let $\mathcal{A} = \{\text{a}, \text{b}, \text{c}\}$ with $P(\text{a}) = 0.2$, $P(\text{b}) = 0.3$, $P(\text{c}) = 0.5$.

Each sequence of type $(n_a, n_b, n_c) = (2,1,3)$ has length 6 and probability
$$
(0.2)^2 (0.3)^1 (0.5)^3 = 0.0015.
$$

There are $\dfrac{6!}{2!\,1!\,3!} = 60$ such sequences.

The probability $\mathbf{x}$ is of type $(2,1,3)$ is $(0.0015) \cdot 60 = 0.09$.

Study probabilities at the level of *types* (most likely, average/typical)