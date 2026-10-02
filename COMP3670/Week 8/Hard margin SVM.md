Assume both classes occur, and that the dataset is linearly separable.
We require every functional margin to be at least $1$. - Every point is on the correct size and has [[Affine score]] of 1. 

We want to minimize $\frac{1}{2}(\langle \mathbf{w},\mathbf{x}_{i} \rangle+b)\geq {1}$
These constraints guarantee a geometric margin of at least $\frac{1}{ \lVert \mathbf{w} \rVert_{2}}$


### Proposition 
Hard margin SVM maximises geometric margin 
At an optimum, $min_{i}y_{i}f_{\mathbf{w},b}(\mathbf{x}_{i})=1$, $\gamma=\frac{1}{\lVert \mathbf{w} \rVert_{2}}$

Support vectors satisfy $y_{i}f_{\mathbf{w},b}=1$
They lie on $f_{\mathbf{w},b}(\mathbf{x})=1$, or $-1$ 
The two margin boundaries are $\frac{2}{\lVert \mathbf{w} \rVert_{2}}$ apart. 
