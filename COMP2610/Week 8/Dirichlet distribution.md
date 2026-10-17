# Background 

Recall [[the Bernoulli distribution]], and in particular, the below section on bayesian inference 
![[Parameter estimation#Bayesian version]]

## Continuing
We use the $Beta(\theta|m_{h},m_{t})$ as a prior for $Bern(x|\theta)$
Our posterior after $n_{h}$ heads, and $n_{t}$ tails is given by $Beta(\theta|m_{h}+n_{h},m_{t}+n_{t})$, and the expected value of $\theta$ under the posterior is $$p(x=h|n_{h},n_{t},m_{h},m_{t})=\frac{m_{h}+m_{t}}{m_{h}+n_{h}+m_{t}+n_{t}}$$
# Definition 
A [[Dirichlet distribution]] is a generalisation of the Beta distribution, to more than two outcomes. 
Its parameter count is a vector $\mathbf{m}$, which can be viewed as "virtual counts" for each symbol $a_{1},\dots,a_{k}$. $$p(x=a_{i}|x_{1}\dots x_{n})= \frac{\#(a_{i})+m_{i}}{\sum_{k=1}^K \#(a_{k})+m_{k}}$$
We implement an adaptative guesser by just counting symbols frequencies. This, unlike every other symbol code, does not require a fixed distribution. 

# Generating code 
The process is almost identical to the one outlined in [[Arithmetic coding#Generating codewords]]
We outline how to create the intervals. 
We fix the probability for end of stream, say $p(\square)=0.15$
We then split up $p(a)=0.425,p(b)=0.425$ Our counts of each are $(1,1)$
when given the first element, say $b$, we get counts $(1,2)$, given $p(a|b)=0.85 \times \frac{1}{1+2}=0.28$, and $p(b|b)=0.85 \times \frac{2}{3}=0.57$
From here, we split up the $b$ interval. 
$ba$ = $0.425, 0.425 +0.425*0.28$
$bb$ width = $0.425*0.57$ 
