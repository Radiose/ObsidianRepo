In regular gradient descent, the gradient is treated as an average over the entire dataset. This can be quite computationally demanding, and we have alternative methods that are a bit more lossy.  

For example, if you had 10000 houses and you wanted to output whether the market is safe or something, you actually have a function $\mathbb{R}^{10000} \to \mathbb{R}$ where the codomain is the error. 
# Statistical background 
Given a list of indices from $\{ 1,\dots,N \}$, and using $\mathbf{g}=\nabla \ell_{i}\theta$ in place of the full gradient 
$\mathbb{E}[\mathbf{g}]= \sum_{i=1}^N \frac{1}{N} \nabla \ell_{i}(\theta)= \nabla J(\theta)$
An improvement is to choose a subset $B = \{ 1,\dots,b \}\subseteq\{ 1,\dots,N \}$ and average $\mathbf{g}=\frac{1}{b} \sum_{i \in B}\nabla \ell_{i}\theta$. It is still unbiased, and like any mean, it will be more stable as $B$ grows
$b=N$ is regular [[gradient descent]], while $b=1$ is the cheapest, and noisiest. 

The trade is that for the price of one exact gradient, we can afford $\frac{N}{b}$ noisy ones, and move $\frac{N}{b}$ steps. 


# In practice 
![[Pasted image 20261031123025.png]]
The image above shows gradient descent vs SGD in $2$ dimensional space (parameters), with $N=100$ observations. 
We need 15 steps for regular GD, for a total of 1500 gradients. 
However, SGD, with b=1,  will need 150 steps, so only 150 gradients. 