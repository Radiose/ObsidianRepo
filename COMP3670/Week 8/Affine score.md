A weight [[vector]] $w \in \mathbb{R}^d$ and a bias $b \in \mathbb{R}$ give the score $$f_{\mathbf{w},b}(\mathbf{x})=\langle \mathbf{w,x} \rangle+b $$
The classifier $y(\mathbf{x})$ predicts 1 for nonnegative $f$, and $-1$ for negative.
# Decision boundary 
when $\mathbf{w}\not=0$,the [[Affine score|affine]] hyperplane $\mathcal{H}=\{ \mathbf{x \in \mathbb{R}^d| \langle \mathbf{w,x} \rangle}+b=0 \}$
Its normal vector (90 degrees) is $\mathbf{w}$. 

If $\mathbf{u,v}\in \mathcal{H}$, then $\langle \mathbf{w},\mathbf{u}\mathbf{-v} \rangle$=$-b-(-b)=0$
Then, $\mathbf{w}$ is perpendicular to every displacement along the boundary.


![[Pasted image 20261002084838.png]]
![[Pasted image 20261002084856.png]]
So as we can see above, we see our $\mathbf{w}$ is perpendicular to everything along the line. 

