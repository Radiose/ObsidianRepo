The general idea here is to break up feature space into a [[partition]] and let each subset of feature space be determined by the majority vote. 

$$W_i(\mathbf{x}) =\begin{cases}\dfrac{1}{k}, & \mathbf{X}_i \text{ is among the } k \text{ nearest neighbours of } \mathbf{x} \\0, & \text{otherwise}\end{cases}$$


$\hat{h}$ assigns each cell the majority label of the training points within it. It is constant on each cell.
In the cubic histogram rule, $I$ is the side of the cubes that make up the grid, and $I$ is the smoothing parameter. 

![[Pasted image 20260827092530.png]]


