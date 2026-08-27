$$
\hat{h}(\mathbf{x}) = \dfrac{\sum_{i=1}^{N} \kappa\!\left(\dfrac{\mathbf{x} - \mathbf{X}_i}{\sigma}\right) Y_i}{\sum_{i=1}^{N} \kappa\!\left(\dfrac{\mathbf{x} - \mathbf{X}_i}{\sigma}\right)} = \sum_{i=1}^{N} W_i(\mathbf{x}) \, Y_i
$$

- **The weights $W_i(\mathbf{x})$ are exactly those of kernel classification**; only what is averaged changed: the labels $\mathbb{1}\{Y_i = 1\}$ there, the numbers $Y_i$ here
- Same kernels, same bandwidth: small $\sigma$ overfits, large $\sigma$ flattens everything towards the average of $Y$
- Using "the [[k nearest neighbour classification|k nearest neighbour]]" instead gives $k$**NN regression**: the average $Y$ of the $k$ closest observations
![[Pasted image 20260827152211.png]]