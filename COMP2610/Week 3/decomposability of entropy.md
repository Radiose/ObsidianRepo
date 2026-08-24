# Example for motivation 
Let us illustrate with an example:

Let $X \in \{ 1,2,3 \}$ be some [[random variable]] determined by a fair process.
Flip a fair coin to determine whether $X=1$.
If $X\not=1$, flip another coin to determine whether $X=2,3$
The probability distribution of the coin:
$P(X=1)=0.5$
$P(X=2)=0.25$
$P(X=3)=0.25$

Typically, we would just use the entropy formula 
$H(X)=H(p)=\frac{1}{2}\log 2+\frac{1}{2}\log(4)+\frac{1}{4}\log(4)=1.5$
But, we can decompose this entropy sequentially. 

First, we learn whether $X=1$
$H\left( \frac{1}{2} \frac{1}{2} \right)=\log_{2}2=1$ bit 
Then, if $X\not=1$, we learn the value of the second coin flip 
$H\left( \frac{1}{2} \frac{1}{2} \right)=1$ bit, BUT, it will only happen $50$% of the time. 
Thus, we obtain $H\left( \frac{1}{2} \frac{1}{2} \right) + \frac{1}{2}\left( H\left(  \frac{1}{2} \frac{1}{2} \right) \right)=1.5$ bits. 

### In general 

For a random variable with probability distribution $\mathbf{p}=(p_{1},\dots p_{\mathcal{X}})$, $H(\mathbf{p})=H((p_{1},1-p_{1}))+(1-p_{1})H\left( \left( \frac{p_{2}}{1-p_{1}},\dots, \frac{p_{\mathcal{X}}}{1-p_{1}} \right) \right)$

Basically, the first term = is $X=1$?
Then, probability $X\not=1$ 
Then, in the $H$ is the [[Bayes theorem|bayesian inference]] for probability of $p_{i}$ given $X\not={1}$
