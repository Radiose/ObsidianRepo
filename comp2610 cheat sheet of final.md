# Run down of everything

# Probability theory

Our variance is $var(X)=\mathbb{E}(X^2)-(\mathbb{E}[X])^2$
$stdv=\sqrt{ var }$


Bayes theorem: Given a *prior* $p(s)$, evidence, $p(x)$ and likelihood $p(x|s)$, we aim to obtain a posterior$p(s|x)$ that we can use to update priors.

The chain rule: This is a method to decompose joint probabilities
$p(X_{1},X_{2},\dots,X_{n})=p(X_{1})p(X_{2}|X_{1})p(X_{3}|X_{2},X_{1})\dots.,p(X_{n}|X_{n-1},\dots,X_{1})$
Also, the marginal probabilities can be obtained by summing up all joint probabilities with respect to the desired variable.
The general rule for conditional probability: $p(A|B)= \frac{p(A \cap B)}{p(B)}$.

Independence: gives $p(X,Y)=p(X)p(Y)$
and $X \mathrel{\perp\!\!\!\perp}Y$ denotes independence between $X$ and $Y$
Conditional independence: $X \mathrel{\perp\!\!\!\perp}Y|Z \iff p(X,Y|Z)=p(X|Z)p(Y|Z)$ 



# Bernoulli and binomial 

The bernoulli distribution: Basically just a coin toss. Our parameter $\theta$ represents the probability of obtaining a $X=1$. By definition, $p(X=1|\theta)=\theta$, $p(X=0|\theta)=1-\theta$ - not quite conditional probability in the traditional sense, more of given this parameter. More succinctly, $p(X=x|\theta)=\theta^x(1-\theta)^{1-x}$

The binomial distribution is a model of some set amount $N$ **independent** Bernoulli trials. 
If $Y = \sum_{i=1}^{N}X_{i}$, where $X_{i}\textasciitilde bern(\theta)$, then $Y$ has a binomial distribution, with parameters $N,\theta$
$p(Y=m)=Bin(m|N,\theta)=\begin{pmatrix}N  \\  m\end{pmatrix}\theta^m(1-\theta)^{N-m}$ - the probability he will get m/N successes.
$\mathbb{E}[Y]=N\theta$, $var[Y]=N\theta(1-\theta)$


Likelihood function: Given a sequence $\mathcal{D}=\{ 0,0,0,1,0,0,1,0,0,0 \}$
We have $p(\mathcal{D}|\theta)=\prod_{i=1}^{10}p(x_{i}|\theta)$
Or more generally $\prod_{i=1}^N \theta^{x_{i}}(1-\theta)^{1-x_{i}}$
Putting it in logs, $\mathcal{L}(\theta)=\log p(\mathcal{D}|\theta)=\sum_{i=1}^N[x_{i}\log \theta+(1-x_{i})\log(1-\theta)]$
The derivative of this at $0$ ends up with the parameter being the proportion of successful trials, which obviously makes sense.

# COME BACK TO BETA PRIOR 

# Information content:
for an outcome of a random variable, its information content is:
$h(x)=\log_{2} \frac{1}{p(x)}$ - can be any log base but we like to use 2

# Entropy 
Average information content of a random variable.
$H(X)=\mathbb{E}_{x}[h(x)]= \sum_{x}p(x)\cdot \log_{2} \frac{1}{p(x)}=- \sum_{x}p(x)\log_{2}p(x)$
Properties: $H(X)\geq 0$


![[Pasted image 20261113145428.png]]




# Entropy 
