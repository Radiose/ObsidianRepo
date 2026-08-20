This is where we assume the distribution has some fixed shape, fixed by a few unknown numbers. We estimate the numbers, and plug them in. Assuming a shape means that not much data is necessary.

# Definition 
A parametric, statistical model is a family of distributions $\{ p(\cdot |\theta)\theta \in \Theta \subset \mathbb{R}^m\}$ indexex by finitely many numbers $\theta=(\theta_{1},\dots,\theta_{m})$ To assume the model is to assume that the unkown distribution is $p(\cdot | \theta^*)$ for some unknown $\theta^* \in \Theta$. 

Some examples are [[the Bernoulli distribution]], and [[The normal distribution]].
- $Y \sim \text{Bernoulli}(\theta)$ if $\mathbb{P}(Y=1) = \theta$ and $\mathbb{P}(Y=0) = 1-\theta$ with $\Theta = [0,1]$
- $Y \sim \text{Normal}(\mu, \sigma^2)$ with $\theta = (\mu, \sigma^2)$ and $\Theta = \mathbb{R} \times \mathbb{R}_+$


Parametric means all our ignorance about the distribution is confided to finitely many numbers. 

Based on these, we can create a parametric plug in rule. We have three steps.
1: choose a family of distributions 
2: estimate the [[Parameter estimation|parameters]] from our data
3: substitute into the rule for $f^*$


