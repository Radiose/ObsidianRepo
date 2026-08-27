Both [[k nearest neighbour classification]] and general [[Histogram classification]] give equal weight to the voters, and zero to everyone else. 

Kernel rules let us decay the weight smoothly with distance.

A kernel is a non negative rule $k: \mathbb{R}^d \to \mathbb{R}$, usually decreasing in $||x||$. If a kernel depends on its input only through its norm, its called a radial bias function.

A kernel induces the weights 

$$W_i(\mathbf{x}) = \dfrac{\kappa\!\left(\dfrac{\mathbf{x} - \mathbf{X}_i}{\sigma}\right)}{\sum_{j=1}^{N} \kappa\!\left(\dfrac{\mathbf{x} - \mathbf{X}_j}{\sigma}\right)}$$
Every observation votes, with a strength that fades with distance. $\sigma$ is the bandwidth, or the smoothing parameter. It sets the distance over which the fading happens.
The denominator ensures the weights sum to $1$. 

![[Pasted image 20260827093612.png]]



![[Pasted image 20260827093716.png]]

$\sigma=1$ is close to optimal, as it is increased we begin to underfit. 
