Probability rules 

# relationship between joint, marginal and conditional probability 


All three of these probability types are intrinsically linked. 
Using the image below as a guide:
![[Pasted image 20260728150326.png]]
Note that $N$ = the sum of all $n_{ij}$

[[marginal probability]] from [[Joint probability]]:
$P(X=x_{i})=\frac{\sum_{j}n_{ij}}{N}$
$=\sum_{j}P(X=x_{i},Y =y_{j})$ - basically the probability of $x_{i}$ with all $y_{j}$

[[Conditional probability]] formula derivation
$$p(Y = y_j \mid X = x_i) = \frac{n_{ij}}{c_i} = \frac{n_{ij}/N}{c_i/N}$$

$$= p(X = x_i, Y = y_j) / p(X = x_i)$$


# The sum rule 

## Axiom
If events $E_{1}\dots E_{n}$ are mutually disjoint, then $\mathbb{P}(E_{1} \cup \dots \cup E_{n})=\mathbb{P}(E_{1})+\dots+\mathbb{P}(E_{n})$
Disjoint events exclude each other, in the sense that they cannot happen at the same times. 

## marginalisation
This is how we use the sum rule to give us [[marginal probability]] from [[Joint probability]]
$p(X = x_i) = \sum_j p(X = x_i, Y = y_j)$
By definition, the sum items must be mutually disjoint. 

### Taking it further
To remove a random variable, or marginalise it you use the sum rule. 

Given $D$ random variables $X_1, \dots, X_D$:

$$p(X_1, \dots, X_{i-1}, X_{i+1}, \dots, X_D) = \sum_{X_i} p(X_1, \dots, X_D)$$





# The product rule 
If events $E_{1},\dots, En$ are **independent** of each other, then the composite probability of $E_{1}$ and $E_{2}$... and$E_{n}$ is 
$\mathbb{P}(E_{1})\times \mathbb{P}(E_{2})\times\dots \mathbb{P}(E_{n})$

The sum and product rules are often combined together. What is the chance of X and Y or Z and W? product rule of X times Y, Z times W, then sum rule them together. 

Suppose you run $n$ experiments with sample spaces $S_{1},S_{2}\dots S_{n}$. For each $1 \le i \le n$, let $E_{i} \in S$ be an event. If the events $E_{1}\dots E_{n}$ are independent of each other, then the probability of composite event $E_{1}$ *and* $E_{2}$ ... *and* $E_{n}$ is $\mathbb{P}_{s_{1}\times s_{2}\times\dots \times s_{n}}(E_{1} \times E_{2} \dots \times E_{n})$ = $\mathbb{P}_{s_{1}}(E_{1})\times \mathbb{P}_{s_{2}}(E_{2})\times\dots \times \mathbb{P}_{s_{n}}(E_{n})$

## Without independence 

**Product Rule:**

$$p(X = x_i, Y = y_j) = p(Y = y_j \mid X = x_i)\, p(X = x_i)$$

and by symmetry:

$$P(Y = y_j, X = x_i) = p(X = x_i \mid Y = y_j)\, p(Y = y_j)$$

Therefore:

$$P(X = x_i) = \sum_j P(X = x_i, Y = y_j) = \sum_j P(X = x_i \mid Y = y_j)\, P(Y = y_j)$$
Here, events do not have to be independent of each other. 

## **Chain Rule:** 

We can also express:

$$p(X_1, X_2) = p(X_1)\,p(X_2 \mid X_1)$$
into 
$$p(X_1, X_2, X_3) = p(X_1, X_2)\,p(X_3 \mid X_1, X_2) = p(X_1)\,p(X_2 \mid X_1)\,p(X_3 \mid X_1, X_2)$$

$$p(X_1, \dots, X_D) = p(X_1)\,p(X_2 \mid X_1)\,p(X_3 \mid X_2, X_1) \cdots p(X_D \mid X_1, \dots, X_{D-1})$$
Here, we are just using the product rule to obtain [[Joint probability]] from [[Conditional probability]].
