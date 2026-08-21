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

![[Parameter estimation#Maximum likelihood estimation]]
![[Parameter estimation#Comp3670]]


# using in classification 
We do not need to know all of $P$, we only need the [[conditional distribution]]. 

We must have $\eta$ in \[0,1] and be a function of $x$. If we try to use some linear function, we get something not in our interval \[0,1].

As a consequence, we transform the probability using a logit of it. 
$logit(p)=\log \frac{p}{1-p}$, which transform a probability in $(0,1)$ to the real line. Small become negative, large become positive 

We create a model using the weighted score of the features with $\mathbf{\theta}=(w_{0},w_{1}\dots w_{d})$

**The model**: the logit is a weighted score of the features with $\theta = (w_0, w_1, \ldots, w_d)$,

$$
\log \frac{\eta(\mathbf{x} \mid \theta)}{1 - \eta(\mathbf{x} \mid \theta)} = \sum_{j=1}^{d} w_j x_j + w_0 
\quad \Longleftrightarrow \quad 
\eta(\mathbf{x} \mid \theta) = \frac{1}{1 + e^{-\left(\sum_{j=1}^{d} w_j x_j + w_0\right)}}$$


![[Pasted image 20260821090735.png]]
Above is the logit curve. The sign of the weight $w_{j}$ says whether the probability of class 1 increases or decreases with variable $j$, with its magnitude saying how sharply. 

Every individual has their own probability of $Y=1$, with the model tying these probabilities together through the same d+1 numbers $\theta$


- So the likelihood of the observed labels is

$$
\mathcal{L}(\theta) = \prod_{i=1}^{N} \eta(\mathbf{X}_i \mid \theta)^{Y_i} \left(1 - \eta(\mathbf{X}_i \mid \theta)\right)^{1-Y_i}
$$

each factor being $\eta(\mathbf{X}_i)$ when $Y_i = 1$, and $1 - \eta(\mathbf{X}_i)$ when $Y_i = 0$

- Taking logarithms gives the **log-likelihood** (recall the properties of logarithms!)

$$
\text{LL}(\theta) = \log \mathcal{L}(\theta) = \sum_{i=1}^{N} \Big[ Y_i \log \eta(\mathbf{X}_i \mid \theta) + (1-Y_i) \log\left(1 - \eta(\mathbf{X}_i \mid \theta)\right) \Big]$$
The product is the logarithm of sums. Then we can just maximise the logarithm. This is the same as minimising $-\frac{LL}{N}$.


(This is basically what we do in [[Parameter estimation]].)


![[cross entropy loss]]


# The hypothesis set 

Our [[hypothesis set]] is basically just the perception. 

# The big picture 
Modelling $\eta$ allows us to differentiate between an input that barely passes a threshold, vs not passing. We can create our own threshold, which allows us to further differentiate, rather than just binary loss constant threshold of $\frac{1}{2}$
