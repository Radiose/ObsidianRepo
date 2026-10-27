---
aliases:
  - support vectors
---
Assume both classes occur, and that the dataset is linearly separable.
We require every functional margin to be **at least $1$**. - Every point is on the correct size and has [[Affine score]] of 1. 

These constraints guarantee a geometric margin of at least $\frac{1}{ \lVert \mathbf{w} \rVert_{2}}$
Hard margin SVM maximises geometric margin (see prop 1)


# Definition 
The hard margin support vector machine chooses $\mathbf{w}\in \mathbb{R}^d\quad  b \in \mathbb{R}$ to solve 

minimize $\frac{1}{2}\lVert \mathbf{w} \rVert_{2}^2$
	subject to $y_{i}(\langle \mathbf{w},\mathbf{x}_{i} \rangle+b)\geq 1\quad (i=1,\dots,n)$

At an optimal solution, training datapoints satisfying $y_{i}(\langle \mathbf{w},\mathbf{x}_{i} \rangle+b)=1$ are called **support vectors**
They lie on the two margin boundaries $(\langle \mathbf{w}_{i},\mathbf{x}_{i} \rangle+b)= 1$ and $(\langle \mathbf{w}_{i},\mathbf{x}_{i} \rangle+b)= -1$


Also known as $y_{i}f_{\mathbf{w},b}=1$

The two margin boundaries are $\frac{2}{\lVert \mathbf{w} \rVert_{2}}$ apart. 


# Proposition 
For a linearly separable dataset containing both classes, the hard margin SVM is equivalent to maximising the geometric margin. 

At an optimum, $\min_{i=1,\dots,n}\ y_{i} (\langle \mathbf{w}_{i},\mathbf{x}_{i} \rangle+b)=1$, $\gamma=\frac{1}{\lVert \mathbf{w} \rVert_{2}}$
This is because this will at the same time able to ensure perturbations (or noise) for future samples wont be too far away.