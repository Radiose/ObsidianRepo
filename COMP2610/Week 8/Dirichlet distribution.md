# Background 

Recall [[the Bernoulli distribution]], and in particular, the below section on bayesian inference 
![[Parameter estimation#Bayesian version]]

## Continuing
We use the $Beta(\theta|m_{h},m_{t})$ as a prior for $Bern(x|\theta)$
Our posterior after $n_{h}$ heads, and $n_{t}$ tails is given by $Beta(\theta|m_{h}+n_{h},m_{t}+n_{t})$, and the expected value of $\theta$ under the posterior is $$p(x=h|n_{h},n_{t},m_{h},m_{t})=\frac{m_{h}+m_{t}}{m_{h}+n_{h}+m_{t}+n_{t}}$$
# Definition 
A [[Dirichlet distribution]] is a generalisation of the Beta distribution, to more than two outcomes. 
