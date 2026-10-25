Recall [[the Bernoulli distribution]], and in particular, the below section on bayesian inference 
![[Parameter estimation#Bayesian version]]

## Continuing
We use the $Beta(\theta|m_{h},m_{t})$ as a prior for $Bern(x|\theta)$
Our posterior after $n_{h}$ heads, and $n_{t}$ tails is given by $Beta(\theta|m_{h}+n_{h},m_{t}+n_{t})$, and the expected value of $\theta$ under the posterior is $$p(x=h|n_{h},n_{t},m_{h},m_{t})=\frac{m_{h}+m_{t}}{m_{h}+n_{h}+m_{t}+n_{t}}$$
# Definition 
A Dirichlect distribution is a generalisation of the Beta distribution, to more than two outcomes. 
Its parameter count is a vector $\mathbf{m}$, which can be viewed as "virtual counts" for each symbol $a_{1},\dots,a_{k}$. $$p(x=a_{i}|x_{1}\dots x_{n})= \frac{\#(a_{i})+m_{i}}{\sum_{k=1}^K \#(a_{k})+m_{k}}$$
We implement an adaptative guesser by just counting symbols frequencies. This, unlike every other symbol code, does not require a fixed distribution.