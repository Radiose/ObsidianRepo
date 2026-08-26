# Motivation 
1000 students sit a test 
The average is $\frac{40}{100}$ 
The principle wants to know the maximum number of students who scored over 80
Call $x$ the number who scored over 80 
$s$ is the number who scored less than or equal to 80
We know $40 \cdot{1}000-S=\{ \text{total score of students who score above 80} \} > 80x$

Exam scores are nonnegative, so $S \geq {0}$
Thus, $80x < 40 \times {1}000 \implies x <500$ 

# Definition 
Let $X$ be a nonnegative [[random variable]]. Then, for any $\lambda>0$, $$P(X \geq \lambda)\leq \frac{\mathbb{E}[X]}{\lambda}$$
### Proof 
$$
\begin{aligned}
\mathbb{E}[X] &= \sum_{x \in \mathcal{X}} x \cdot p(x) \\
&= \sum_{x < \lambda} x \cdot p(x) + \sum_{x \geq \lambda} x \cdot p(x) \\
&\geq \sum_{x \geq \lambda} x \cdot p(x) && \text{(nonneg. of random variable)} \\
&\geq \sum_{x \geq \lambda} \lambda \cdot p(x) \\
&= \lambda \cdot p(X \geq \lambda)
\end{aligned}
$$
