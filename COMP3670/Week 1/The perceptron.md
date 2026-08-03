---
aliases:
  - PLA
---
This is one of the simplest ML models 
We fix the [[hypothesis set]] accordingly:
$\mathcal{H}$ = the set of linear threshold functions. 

Binary [[classification]]: $\mathcal{Y}=\{ +1,-1 \}$, features $\mathbf{x}=(x_{1},\dots,x_{n}) \in \mathcal{X}=\mathbb{R}^n$= all [[vector]]s of $n$ real numbers. 

Each hypothesis in $\mathcal{H}$ has the form $h_{w}(x) =\text{sign}(w_{1}x_{1}+w_{2}x_{2}+\dots+w_{n}x_{n}+w_{0})$ - we take in some weighted sum of the inputs, and output according to the sign. $+1$ if sign > 0 and -1 if      sign $\leq 0$. $\mathbf{w}=(\mathbf{w}_{0},\mathbf{w}_{1}\dots+\mathbf{w_{n}})$. 

We formally define $\mathcal{H}=\{ h_{w}:w_{0},w_{1}\dots w_{n}\in \mathbb{R} \}$, or the set of all possible weights. 
$|\mathcal{H}|=\infty$.


## Geometric interpretation 
We can interpret the perceptron model geometrically(at least for $\mathbb{R}^n\ n\leq {3}$)
Take the two dimensional case $w_{1}x_{1}+w_{2}x_{2}+w_{0}$
It effectively splits $\mathbb{R}^2$ into an $h =+1$ and $h=-1$ region. 
![[Pasted image 20260803123701.png|489]]
for $\mathbb{R}^n$, we call this a hyperplane. 


We claim that a training example $(\mathbf{x_{1}},y_{1})$ to be misclassified when $sign(w_{1}x_{1}+w_{2}x_2+\dots+w_{n}x_{n}+w_{0})\not=y_{i}$
We need an algorithm to search for such weights automatically. 
The idea for the algorithm is:
1: initialise $w_{1}(0)=\dots=w_{n}(0)=w_{0}(0)=0$
2: For each iteration $t=1,2\dots$, 
	find any misclassified training example $\mathbf{x_{i}},y_{i}$
	Update for $j=1,..,n$ $$w_{j}(t)\leftarrow w_{j}(t-1)+y_{i},\mathbf{x}_{ij}\quad w_{0}(t)=w_{0}(t-1)+y_{i}$$
## Example

Consider two training points:

$$\mathbf{x}_1 = (1,1), \quad y_1 = +1 \qquad \mathbf{x}_2 = (-1,-1), \quad y_2 = -1$$

- Initialise: $w_1 = 0$, $w_2 = 0$, $w_0 = 0$
- Score for $\mathbf{x}_1 = (1,1)$:

$$w_1 x_{1,1} + w_2 x_{1,2} + w_0 = 0 \cdot 1 + 0 \cdot 1 + 0 = 0$$

- A score of $0$ counts as $-1$, hence this point is misclassified
- We will update the weights using this point

- Update using $(\mathbf{x}_1, y_1) = ((1,1), +1)$:

$$w_1 \leftarrow 0 + (+1) \cdot 1 = 1$$
$$w_2 \leftarrow 0 + (+1) \cdot 1 = 1$$
$$w_0 \leftarrow 0 + (+1) = 1$$

- New weights: $w_1 = 1$, $w_2 = 1$, $w_0 = 1$
- Score for $\mathbf{x}_2 = (-1,-1)$ with the updated weights:

$$1 \cdot (-1) + 1 \cdot (-1) + 1 = -1$$

- $\text{sign}(-1) = -1 = y_2$, which is **correctly classified**
- Re-check $\mathbf{x}_1 = (1,1)$ with the updated weights:

$$1 \cdot 1 + 1 \cdot 1 + 1 = 3 > 0$$

- $\text{sign}(3) = +1 = y_1$, which is **correctly classified**
- Both training points are now correctly classified and the PLA **stops** after a single update

# Key result: the [[Convergence of a sequence|converge]] theorem
If the data is linearly separable, then the perceptron learning algorithm is guaranteed to stop after some finite number of updates and return some solution. This is quite a significant result, some simple [[greedy algorithm]] will find the solution if it exists. 

If some solution doesnt exist, then the algorithm will run forever. 
