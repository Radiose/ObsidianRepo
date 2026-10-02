when $\mathbf{w}\not=0$,the [[Affine score|affine]] hyperplane $\mathcal{H}=\{ \mathbf{x \in \mathbb{R}^d| \langle \mathbf{w,x} \rangle}+b=0 \}$
Its normal vector (90 degrees) is $\mathbf{w}$. 

If $\mathbf{u,v}\in \mathcal{H}$, then $\langle \mathbf{w},\mathbf{u}\mathbf{-v} \rangle$=$-b-(-b)=0$
Then, $\mathbf{w}$ is perpendicular to every displacement along the boundary.


![[Pasted image 20261002084838.png]]
![[Pasted image 20261002084856.png]]
So as we can see above, we see our $\mathbf{w}$ is perpendicular to everything along the line. 

# Importance of distance 

Several hyperplanes can classify all points correctly, but a point close to a boundary can change its prediction after a small feature perturbation. Multiplying by $\mathbf{w}$ and $b$ by a positive constant will rescale scores but keep the boundary fixed. 


### Proposition 
For $\mathcal{H}=\{ \mathbf{z}:\langle \mathbf{w,z} \rangle +b=0\}$ the closest point (on the boundary) to $\mathbf{x}$ is given by $\mathbf{p}=\mathbf{x}-\frac{\langle \mathbf{w},\mathbf{x} \rangle+b}{\lVert \mathbf{w} \rVert_{2}^2}\mathbf{w}$


The distance and signed distance are $d(\mathbf{x},\mathcal{H})=\frac{\lvert f_{\mathbf{w},b}(\mathbf{x}) \rvert}{\lVert \mathbf{w} \rVert_{2}}$ and $s(\mathbf{x},\mathcal{H})=\frac{f_{\mathbf{w},b}(\mathbf{x})}{\lVert \mathbf{w} \rVert_{2}}$ 
Note that signed distance is positive on the side with towards which $\mathbf{w}$ points. 

![[Pasted image 20261002091636.png]]
## Functional and geometric margins 
For a labelled datapoint $\mathbf{x}_{i},y_{i}$, define the functional and geometric margin as follows$$m_{i}=y_{i}f_{\mathbf{w},b}(\mathbf{x}_{i}),\quad \gamma_{i}=\frac{m_{i}}{\lVert \mathbf{w} \rVert_{2} }$$Note that 
If $m_{i}>0$, the point is strictly on the correct side, and $m_{i}<0$ implies its strictly on the wrong side.
Multiplying by $y_{i}$ treats both classes the same way.

# Linearly separable
We say a dataset $\mathcal{D}$ is linearly separable, if $$\forall i \in \{ 0,1\dots|\mathcal{D}| \},\exists \mathbf{w},b\text{ such that  } m_{i}>0$$
The margin of a separating classifier is $\gamma=min_{i=1,\dots,n}\ \ \gamma_{i}$

A perturbation $\delta$ with $\lVert \delta \rVert_{2}<\gamma_{i}$ cannot change the prediction for that point. Additionally, a larger training margin does not itself guarantee predictions on unseen data.

![[Support vector machine]]