Recall mutual information 
![[mutual information]] 


In the context of channel capacity, mutual information can be thought of as *how much what was received reduces uncertainty about what was sent*

This requires we specify some particular $p(X)$, where $X$ is the inputs, and $Y$ is the outputs. 
This is achieved through its [[transition matrix]].

## Noiseless [[channel]] example 
For a noiseless channel, $H(X|Y)=0$ IE, there is no added entropy from $X$ onto $Y$.
So, if $p_{X}=(0.9,0.1)$, then we can just easily compute [[mutual information]] ($H(X)-H(Y|X)$).
$\implies I(X,Y)=0.47$

Intuitively, we have that our reliability is *noiseless > Z > symmetric*

# Channel capacity definition
The capacity $C$, of a channel $Q$, is the largest mutual information between its input, and output for **any** choice of input [[ensemble]].
IE $$C = \max_{\mathbf{p}_{X}}I(X;Y)$$We will demonstrate that the capacity determines the rate at which we can communicate across a channel with arbitrarily small error.

# Computing capacity 
The basic rules for computing the channel capacity for a channel $Q$ with inputs $\mathcal{A}_{X}$ and outputs $Y_{X}$ is to:
	1: compute the mutual information $I(X;Y)$ for some general $\mathbf{p}_{X}$
	2: Determine which choice of $\mathbf{p}_{X}$ maximised that mutual information 
	3: Use that maximising value to determine $C$

# Symmetric channels 
![[symmetric channel]]

For symmetric channels, the optimal distribution is achieved with a simple form. 

# Theorem 
If $Q$ is symmetric, then its capacity is achieved by a uniform distribution over $\mathcal{X}$.

# Example 
Computing the capacity of the [[Discrete channel#The binary symmetric channel|the binary symmetric channel]].
$Q=\begin{bmatrix}1-f  &  f \\  f  & 1-f\end{bmatrix}$
We aim to calculate mutual information $H(Y)-H(Y|X)$
We therefore need to calculate the distributions $p(Y)$ and $p(Y|X)$

$p(Y=0)= (1-f) \cdot \mathbb{P}(X=0) \cdot \mathbb{P}(X=1)$
$p(Y=1)= (1-f) \cdot p(x=1)+f \cdot p(x=0)$
This can also be expressed with $\mathbf{q}=Q \mathbf{p}_{X}$, where $\mathbf{p}_{X}$ is the probability vector in the ensemble (returns a vector of $y$ probabilities).

Calculating entropy: 
$H(Y)=- q_{0}\log_{2}q_{0}-q_{1}\log_{2}q_{1}$
$=-q_{1}\log_{2}q_{1}-(1-q_{1})\log_{2}(1-q_{1})$  because ($q_{0}+q_{1}=1$)
=$H_{2}(\mathbf{q}_{1})$ (binary entropy function)
$=H_{2}(f \cdot p_{0}+(1-f)\cdot p_{1})-H_{2}(f)$


**Computing $H(Y|X)$:**

Since $P(y|x)$ is described by the matrix $Q$, we have

$$H(Y|x=0) = H_2\big(P(y=1|x=0)\big) = H_2(Q_{1,0}) = H_2(f)$$

and similarly,

$$H(Y|x=1) = H_2\big(P(y=1|x=1)\big) = H_2(Q_{0,1}) = H_2(f)$$

So,

$$H(Y|X) = \sum_x H(Y|x)\,P(x) = \sum_x H_2(f)\,P(x) = H_2(f)\sum_x P(x) = H_2(f)$$

**Computing $I(X;Y)$:**

Putting it all together gives

$$\boxed{I(X;Y) = H(Y) - H(Y|X) = H_2\big(f \cdot p_0 + (1-f)\cdot p_1\big) - H_2(f)}$$
Because $Q$ is symmetric, we can easily use the uniform distribution property 
![[Pasted image 20261026121400.png]]
as you can see, $I(X;Y)$ is maximised when $p_{1}=0.5$
In which case $C=0.39$ for $f=0.15$
