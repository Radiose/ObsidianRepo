The idea with this is to fix the number of points and let the region adapt 

$\hat{h}(\mathbf{x})$ is the majority label among the $k$ training points closest to $\mathbf{x}$.

$$W_i(\mathbf{x}) = \begin{cases} \dfrac{1}{k}, & \mathbf{X}_i \text{ is among the } k \text{ nearest neighbours of } \mathbf{x} \\ 0, & \text{otherwise} \end{cases}$$

$k=1$ gives the [[Nearest neighbour algorithm]].
$k$ is the smoothing parameter. 
![[Pasted image 20260827092206.png]]


We need to note here that the in sample error is meaningless for small $k$. At $k=1$, it is 0. 
The training set here is the model. Nearest neighbour rules are not just heuristic. For large $N$, the error of the $1NN$ is at most twice the error of the best possible classifier. 
