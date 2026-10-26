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

