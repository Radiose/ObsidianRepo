the target function $f*$ is the function that has the smallest [[out of sample error]]


Let $\eta(\mathbf{x})=\mathbb{E}[Y|\mathbf{X}=\mathbf{x}]$

Then, the target function is 

regression: squared loss $f^*(\mathbf{x})=\eta(\mathbf{x})=\mathbb{E}[Y|\mathbf{X}=\mathbf{x}]$
classification: binary loss $f^*(\mathbf{x})=arg_{y \in \mathcal{Y}}max\ p_{Y|\mathbf{x}}(y|\mathbf{x})$

CLASSIFICATION CLEARER BELOW
![[Pasted image 20260820190350.png]]
# out of sample error of each $f^*$

Theorem:
regression, squared loss: $L(f^*)=\mathbb{E}[\text{var}(Y|\mathbf{X})]$
classification, binary loss: $L(f^*)=\mathbb{E}[min\{\eta(\mathbf{X}),1-\eta(\mathbf{X})  \}]$

This error is irreducible. 

The target function is determine by the [[loss function]] we chose, and the [[conditional distribution]] of $Y$ given $\mathbf{X}$. Being the best doesn't make it perfect. There will typically be some loss. 