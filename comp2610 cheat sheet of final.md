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
For a Bernoulli trial, we can measure the entropy just as $-p\log_{2}(p)-(1-p)\log_{2}(1-p)$
A uniform distribution has maximised its entropy.

Entropy is a lower bound on the average number of bits to transmit the state of a random variable. 

You can decompose entropy as well. 
For a random variable with prob distribution $\mathbf{p}=(p_{1},\dots,p_{\mathcal{X}})$
We can split it up into blocks. Say $\{ 1,\dots,m \},\{ m+1,\dots,|\mathcal{X}| \}$.
$P_{1}$ is the sum of the probabilities of the outcomes in block, with $P_{2}$ defined similarly.
This gives $H(\mathbf{p})=H((P_{1},P_{2}))+P_{1}H\left( \frac{p_{1}}{P_{1}},\dots,\frac{p_{m}}{P_{1}} \right)+P_{2}H\left( \frac{p_{m+1}}{P_{2}},\dots,\frac{p_{|\mathcal{X}|}}{P_{2}} \right)$ 
$\frac{p_{1}}{P_{1}}$ is the probability that $X=1$ given $X$ is in the first block. 

#### Joint and conditional entropy follow similar ideas. 

Conditional:
$H(Y|X)=\sum _{x \in \mathcal{X}}\sum_{y \in \mathcal{Y}}p(x,y) \log_{2} \frac{1}{p(y|x)}$ 


### CHAIN RULE COME BACK

#### [[relative entropy|KL divergence]]/relative entropy 
This is a method of obtaining the "distance" between two probability distributions. If we have the "true" distribution $p$, and our assumed distribution $q$, the $D_{KL}(p ||q)= \sum p(x)\log\left( \frac{p(x)}{q(s)} \right)$
Properties:
$D_{KL}(p ||q)\geq 0$, where equality is obtained iff $p=q$
Note that because we assume a true distribution $p$, no symmetry.
"the penalty of assuming $q$ when $p$ is the true distribution on the minimised expected code length"

#### Mutual information 
The mutual information of two random variables is $I(X;Y)=D_{KL}(p(X,Y)||p(X)p(Y))$
We can also write it as $H(X,Y)-H(X|Y)$. Note that because $I(X;Y)=I(Y;X)$ we can also get it by $H(X,Y)-H(Y|X)$
"how much information on average does $X$ tell us about $Y$" and "the average reduction in the uncertainty of $X$ given the uncertainty of $Y$"

Note that importantly $I(X;Y)=0 \iff X \mathrel{\perp\!\!\!\!\perp}Y$

![[Pasted image 20261113145428.png]]




# Conditional mutual information 

This is $I(X;Y|Z)$ note that we are getting the mutual information between $X$, and $Y$ conditioned on $Z$. Can be simplified as $I(X;Y|Z)=H(X|Z)-H(X|Y,Z)$ (note that this is $[X|(Y,Z)]$)

The reduction in the uncertainty of $X$ due to the knowledge of $Y$ when $Z$ is given. 

Note that $I(X;Y|Z)=I(Y;X|Z)$ and that $I(X|Z;Y)$ is illegal. 

# Joint 
$I(X_{1}X_{2},\dots,X_{n};Y_{1}Y_{2},\dots,Y_{m})=H(X_{1},\dots,X_{n})-H(X_{1},\dots,X_{n}|Y_{1},\dots,Y_{n})$
Symmetry applies to joint. 
We can also write it as $H(X_{1},\dots,X_{n})+H(Y_{1},\dots,Y_{M})-H(X_{1},\dots X_{n};Y_{1},\dots,Y_{m})$
This is because of the entropy chain rule.

## Chain rule for mutual information
$I(X;Y,Z)=I(X;Y)+I(X;Z|Y)$
In total, 
$I(X_{1},\dots,X_{N};Y)=I(X_{1};Y)+I(X_{2};Y|X_{1})+I(X_{3};Y|X_{1}X_{2})+\dots+I(X_{n};Y|X_{1},\dots,X_{n-1})$

# Inequalities:
Jensens inequality 
For convex $f$, with $X$ a random variable, then $f(\mathbb{E}[X])\leq \mathbb{E}[f(x)]$

Markovs inequality 
For any $\lambda>0$ $P(X \geq \lambda)\leq \frac{\mathbb{E}[X]}{\lambda}$

Chebychovs inequality:
For random variables that take negative values, and also more useful because it uses variance 
$p(|X-\mathbb{E}[X]|\geq \lambda)\leq \frac{var[X]}{\lambda^2}$
- useful for estimating how large $n$ should be so that $\hat{\theta}$ is within $\lambda$ of $\theta$ - a form of bound on a generalisation gap. 
Example: 
Estimate how large $n$ should be such that $p(|\hat{\theta_{n}}-\theta|\geq 0.05)\leq 0.01$ (less than 1% chance of 5% error)
Note that $\mathbb{E}[\hat{\theta}_{n}]=\theta$ and $var[\hat{\theta}_{n}]=\frac{\theta(1-\theta)}{n}$ 

Information cannot hurt 
$H(X|Y)\leq H(X)$, (= iff $x \mathrel{\perp\!\!\!\perp}y$

Law of large numbers 
If $\mu=\mathbb{E}(X)$, then $\forall\epsilon$, 
$\lim_{ n \to \infty }p(|\bar{X}_{n}-\mu|>\epsilon)=0$
# ENSEMBLE 
An ensemble is tuple $(X, \mathcal{A}_{X},\mathcal{P}_{X})$
X is a RV, $\mathcal{A}_{X}$, its alphabet is where it takes values, and $\mathcal{P}_{X}$ is the associated probabilities
An extended ensemble is an ensemble where we denote blocks of size $N$. We denote it $X^N$. Outcomes from $X^N$ are denoted $\mathbf{x}=(x_{1},\dots,x_{n})$. The probability of $\mathbf{x}$ is defined to be 
$P(\mathbf{x})=P(x_{1})P(x_{2})\dots p(x_{N})$
For a given type of sequence, the amount of sequences with these symbol counts are:
$$\frac{N!}{n_{1}!n_{2}!\dots n_{I}!}$$
The probability of some sequence containing some non ordered quantity of elements in the alphabet is $p(x_{1})^{n_{1}}p(x_{2})^{n_{2}}\dots$ and then multiply by the corresponding multinomial coefficient. 

The typical set $T_{N\beta}$  of$X^N$, is defined as $\left\{  \mathbf{x}\in X^N| - \frac{1}{N}\log_{2}P(\mathbf{x})-H(X) |<N\beta \right\}$

every $\mathbf{x}\in T_{N\beta}$ has $2^{-N(H(X)+\beta)}\leq P(\mathbf{x})\leq 2^{-N(H(X)-\beta)}$
For any $N,\beta$, $|T_{N\beta}|\leq 2^{N(H(X)+\beta)}$

Note that the most likely sequence may not actually be in the typical set. For example, if we have the probability of heads being $0.75$, then $hhhh$ is the most likely. However, because there is only one copy of it, its unlikely to be in the typical set. The addition of the multinomial coefficient can balance out the exponential decay that occurs with block size increase.

AEP:
If $x_{1},x_{2},\dots$ are IID, with distribution $P$, then 
$\forall\beta>0$,  $\lim_{ N \to \infty }p\left( \left\lvert  -\frac{1}{N} \log_{2}P(x_{1},\dots,x_{N})  \right\rvert<\beta \right)=1$ - as $N$ gets large, pretty much any sequence drawn will be typical. 


# SOURCE CODING 
Informal version of the source coding theorem 
If you want to uniformly code large sequences of outcomes, with any degree of reliability, then the average number of bits you need is roughly equal to the entropy of that source. 

A source code is a function $c: \mathcal{A}_{X} \to \{ 0,1 \}^+$. The length of the codeword of $x$ is the number of symbols in $c(x)$. 

The extension of $c$ is defined as $c(x_{1},\dots,x_{n})=c(x_{1})\dots(x_{n})$ 

Uniform code: $l(x)$ is the same 
variable length code otherwise 

Lossless code: $x_{1} \not= x_{2} \implies c(x_{1})\not=c(x_{2})$ (injectivity)
Lossy otherwise 

Raw bit content of an ensemble: $H_{0}(X)=\log_{2} |\mathcal{A}_{X}|$ - the number of bits required to uniformly code an ensemble. 

Smallest $\delta$ sufficient subset 
The smallest subset of $\mathcal{A}_{X}$ such that $p(\mathcal{x}\in S_{\delta})\geq 1-\delta$ 
-construct by removing elements of $\mathcal{A}_{X}$ in ascending order until threshold has been reached 

The essential bit content: $H_{\delta}(X):= \log_{2}|S_{\delta}|$

Source coding theorem formally: $$\forall\epsilon>0, \forall\delta \in (0,1),\exists N \in \mathbb{N}^+ \forall n>N\quad \left\lvert  \frac{1}{n}H_{\delta}(X^n)-H  \right\rvert<\epsilon$$
For all epsilon, and for all delta between 0,1, there is some natural number $N$ such that for all $n$ greater than $N$, sequences of length $n$ have average essential bit content close to the entropy of the ensemble.

Given a tiny probability of error, we can make the average essential bit content as close as we want to the entropy by making N large. But, even with large error, we cannot compress more than $H$ bits. If you use more than $NH(X)$ blocks per bit, then you can do so with basically no loss, however, if you use less, you will almost certainly lose information. 



# Symbol Coding 
$\mathcal{A}^+:= \bigcup_{N}\mathcal{A}^N$ - the set of all finite strings
A code $c$ for $X$ is uniquely decodable if no two strings from $\mathcal{A}_{X}^+$ have the same codeword. IE, $\forall x,y \in \mathcal{A_{X}^+}$, $\mathbf{x}\not= \mathbf{y}\implies c(\mathbf{x})\not=\mathbf{y}$ - slightly different to lossless which talks about singular symbols while this is more about combinations of symbols.

A codeword $\mathbf{c}\in \{ 0,1 \}^+$ is said to be a prefix of another codeword $\mathbf{c}'$ if $\exists \mathbf{t}\in \{ 0,1 \}^+$ such that 
$\mathbf{c}'=\mathbf{ct}$

Kraft inequality: 
For lengths $\{ \ell_{1},\dots,\ell_{I} \}$ satisfying
$\sum_{i=1}^I 2^{-\ell_{i}}\leq 1$
A prefix code exists with those lengths. 

Expected code length:
$L(C,X)=\sum_{i=1}^I \ell_{i}p_{i}$

Given lengths $\{ \ell_{1},\dots,\ell_{I} \}$
the probabilities for $\ell_{i}$ is $q_{i}=\frac{2^{-\ell_{i}}}{z}$
Where $z$ is the sum of all lengths $\sum_{i}2^{-\ell_{i}}$
Minimising expected code length is by minimising the KL divergence between $p$ and $q$

Shannon codes:
Picking lengths $\ell_{i}=\lceil \log_{2} \frac{1}{p_{i}} \rceil$ gives us optimal expected code lengths

