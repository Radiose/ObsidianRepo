This is where we assume no shape for the distribution, and instead we estimate the distribution by smoothing the data. We look near $\mathbf{x}$ and see which class is in the majority there. 
We gain the ability to produce arbitrarily complicated decision boundaries that for for any distribution, however, this comes at the cost of more data and a real risk of overfitting. 

Our parameter is one that controls how large *near $\mathbf{x}$* is. 

# Example: Histogram 
![[Pasted image 20260821093447.png]]

Here we have a step function. It is not really demonstrative of the actual distribution of the data.
What we want to do is to smooth the data out. 

the kernel idea 
In the histogram, each observation contributes a rectangle over its own bin. 
	The new idea is to let each contribution contribute a small bump centred on itself, and to add the bins up. 

![[Pasted image 20260821093712.png]]

Every observation now influences the estimate everywhere, with strength that fades with distance. 

$k$, the kernel, is the shape of the bump, $\sigma$ is its width. $\sigma$ is also known as the **smoothing** parameter. 

![[Pasted image 20260821093922.png]]

Above we can see the effect of varying $\sigma$.
We want something in the middle, left is overfitting, and right is underfitting. 
We note that we get a [[Density function]] from varying $\sigma$.

# Obtaining the conditional probability 
What we want to do is to get the density of $X$ when $Y$ is equal to 1, and the density when $Y$ is equal to zero via smoothing.




$$
\hat{p}_1(\mathbf{x}) = \frac{1}{N\sigma^d} \sum_{i=1}^{N} \kappa\!\left(\frac{\mathbf{x} - \mathbf{X}_i}{\sigma}\right) \mathbb{1}\{Y_i = 1\}, 
\qquad 
\hat{p}_0(\mathbf{x}) = \frac{1}{N\sigma^d} \sum_{i=1}^{N} \kappa\!\left(\frac{\mathbf{x} - \mathbf{X}_i}{\sigma}\right) \mathbb{1}\{Y_i = 0\}
$$

Summing together, we get the [[Joint probability]], and from there, we can obtain the [[Conditional probability]].


$$
\hat{\eta}(\mathbf{x}) = \frac{\hat{p}_1(\mathbf{x})}{\hat{p}_1(\mathbf{x}) + \hat{p}_0(\mathbf{x})} = \sum_{i=1}^{N} W_i(\mathbf{x}) \mathbb{1}\{Y_i = 1\}, 
\qquad 
W_i(\mathbf{x}) = \frac{\kappa\big((\mathbf{x} - \mathbf{X}_i)/\sigma\big)}{\sum_{j=1}^{N} \kappa\big((\mathbf{x} - \mathbf{X}_j)/\sigma\big)}$$

A density estimate asks how many observations are near $\mathbf{x}$, and the conditional asks what percentage of them carry the label $1$. We smooth labels, not points. 



# The general nonparametric plug in 


$$
\hat{\eta}(\mathbf{x}) = \sum_{i=1}^{N} W_i(\mathbf{x}) \mathbb{1}\{Y_i = 1\}, 
\qquad 
W_i(\mathbf{x}) \geq 0, \quad \sum_{i=1}^{N} W_i(\mathbf{x}) = 1
$$

$$
\hat{h}(\mathbf{x}) = \mathbb{1}\left\{\hat{\eta}(\mathbf{x}) > \tfrac{1}{2}\right\} = \mathbb{1}\left\{ \sum_{i=1}^{N} W_i(\mathbf{x})\mathbb{1}\{Y_i=1\} \; > \; \sum_{i=1}^{N} W_i(\mathbf{x})\mathbb{1}\{Y_i=0\} \right\}
$$

- $W_i(\mathbf{x})$ is the **influence** of observation $i$ on the decision at the point $\mathbf{x}$. The weights depend on $\mathbf{x}$ , and also on where *all* the other observations are

### Visualisation
![[Pasted image 20260827085331.png]]

As you can see, each training point gets a weight $W_{i}(x)$ drawn as a bar that's tall when close to $\mathbf{x}$, and short when far. 

Move $\mathbf{x}$ and the weights change. The classifier is then rebuilt at every points its evaluated. 

### The assumption of non parametric method
We encode an assumption about $P$. 
Points that are close together in feature space, are more likely to belong to the same class than points that are far apart. 



