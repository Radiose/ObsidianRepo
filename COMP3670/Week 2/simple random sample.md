# Motivation
The essential concept of machine learning in the [[supervised learning framework]] is that any data you train on is merely some sample of an entire population. Statistics is the discipline that makes sampling rigorous. 

Importantly, not every sample is informative. The assumption that makes a sample informative is that of a **simple random sample**.

The assumption that makes a simple informative is that the [[random variable]]s are [[Independent event|independent]].
When some random variables are independent, the conditional probability of $p(y|x)=p(y)$.
Remember that this must hold for all values of $X$ and $Y$.

### Example 
Two patients at random from a large population are drawn. Blood pressure is recorded.
If $X_{1},X_{2}$ are independent, then the probability that both have the disease is just $0.1\cdot{0}.1$ (obviously the percentage of disease is $0.1$).

Dependence is an important thing between features and outcomes. We want to measure features to predict outcomes. This is the basis of most of machine learning. 

From here, we get **the definition of a simple random sample**

# Definition 

A simple random sample of size $N$ from a distribution $P$ is a collection of [[random vector]]s $$(\mathbf{X_{1}},Y_{1}),\dots,(\mathbf{X_{n}},Y_{n})$$
that are [[Independent event|independent]], and identically distributed, each with distribution $P$.

The theoretical generalisation guarantees of statistical learning theory depend on the independent, identically distributed assumption. 

# Unseen data 
This is some $(\mathbf{X,Y}) \textasciitilde P$, drawn independently of $(\mathbf{X_{1},}Y_{1}),\dots,(\mathbf{X_{n}},Y_{n})$ 
The requirements:
Must be from the same distribution, and must be [[Independent event|independent]] IE the test point was in no way used to choose the hypothesis. 