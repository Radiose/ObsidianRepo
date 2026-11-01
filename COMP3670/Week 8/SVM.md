---
aliases:
  - support vector machine
---
![[Affine score]]



# Importance of distance 

Several hyperplanes can classify all points correctly, but a point close to a boundary can change its prediction after a small feature perturbation. Multiplying by $\mathbf{w}$ and $b$ by a positive constant will rescale scores but keep the boundary fixed.



### Proposition 
For $\mathcal{H}=\{ \mathbf{z}:\langle \mathbf{w,z} \rangle +b=0\}$ the closest point (on the boundary) to $\mathbf{x}$ is given by $\mathbf{p}=\mathbf{x}-\frac{\langle \mathbf{w},\mathbf{x} \rangle+b}{\lVert \mathbf{w} \rVert_{2}^2}\mathbf{w}$


The distance and signed distance are $d(\mathbf{x},\mathcal{H})=\frac{\lvert f_{\mathbf{w},b}(\mathbf{x}) \rvert}{\lVert \mathbf{w} \rVert_{2}}$ and $s(\mathbf{x},\mathcal{H})=\frac{f_{\mathbf{w},b}(\mathbf{x})}{\lVert \mathbf{w} \rVert_{2}}$ 
Note that signed distance is positive on the side with towards which $\mathbf{w}$ points. 

![[Pasted image 20261002091636.png]]
## Functional and geometric margins 
For a labelled datapoint $\mathbf{x}_{i},y_{i}$, define the functional and geometric margin as follows$$m_{i}=y_{i}f_{\mathbf{w},b}(\mathbf{x}_{i}),\quad \gamma_{i}=\frac{m_{i}}{\lVert \mathbf{w} \rVert_{2} }$$If $m_{i}>0$, the point is strictly on the correct side, and $m_{i}<0$ implies its strictly on the wrong side. The geometric margin is the datapoints distance to the boundary with these signs. 

Multiplying by $y_{i}$ treats both classes the same way.




# Linearly separable
We say a dataset $\mathcal{D}$ is linearly separable, if $$\exists \mathbf{w},b\text{ such that  } \forall i \in \{ 0,1\dots|\mathcal{D}| \} m_{i}>0$$Read as: There is some weight and bias that can correctly classify all points in the dataset.

The margin of a separating classifier is $\gamma=min_{i=1,\dots,n}\ \ \gamma_{i}$

The geometric margin additionally gives a direct robustness representation.

A perturbation $\delta$ with $\lVert \delta \rVert_{2}<\gamma_{i}$ will give $$y_{i}f_{\mathbf{w,b}}(\mathbf{x}_{i}+\delta)=m_{i}+y_{i}\langle \mathbf{w},\delta \rangle \geq m_{i}-\lVert \mathbf{w} \rVert _{2}\lVert \delta \rVert _{2}>0 $$via Cauchy schwarz inequality.
Thus, its prediction cannot change under such a perturbation.

A larger training margin does not itself guarantee predictions on unseen data, but the robustness property gives a reason to prefer a separator that doesn't pass too close to training points. 

# Types of SVM 

**A support [[vector]] machine maximises the margin $\gamma$** 

# Hard Margin 
![[Hard margin SVM]]
