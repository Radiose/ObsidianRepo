In real training data, overlapping classes, measurement errors or incorrect labels can appear. Then, no hyperplane may satisfy all the [[Hard margin SVM|hard margin]] constraints. Even when strict separation is possible, one unusual datapoint can force a very narrow margin. 

A soft margin SVM allows violations **but charges for them**, balancing the preferences for a wide margin against the fit to the labelled data. 


# Definition 
Fix some parameter $C>0$
The soft margin support vector aims to:
- minimise $\frac{1}{2} \lVert  \mathbf{w} \rVert^2_{2}+C \sum_{i=1}^n \xi_{i}$
- subject to $y_{i}(\langle \mathbf{w},\mathbf{x}_{i} \rangle+b) \geq 1-\xi\quad i=(1,\dots,n)$
		 $\xi_{i}\geq 0$ for $i=1,\dots,n$

$\xi_{1},\dots,\xi_{n}$ are slack variables. 
Each $\xi_{i}$ permits a violation of one datapoints unit functional-margin requirement.
note that with soft SVM, we permit $\mathbf{w}=\mathbf{0}$, giving a constant score

### Hinge loss 
Recall $m_{i}=y_{i}(\langle \mathbf{w},\mathbf{x}_{i} \rangle+b)$
$m_{i}>0$ means correctly classified
$m_{i}<0$ means incorrect 
$m_{i}=0$ means its on the decision boundary

The **hinge loss** of a labelled score of functional margin $m_{i}$ is $\ell(m_{i})=\max\{ 0,1 -m_{i}\}$
For a fixed $\mathbf{w},b$ the constraints require $\xi_{i}\geq {0},$ and $\xi_{i}\geq 1-m_{i}$

Since $C>0$, the best choice is the smallest permitted value $\xi_{i}=\max\{ 0,1-m_{i} \}=\ell(m_{i})$


Using that $\xi_{i}$ definition, the following can be useful

![[Pasted image 20261101144504.png]]

If $\xi=0$, then $m_{i}>1$ and thus is out of the margin, and correctly classified 
if $\xi_{i}\in(0,1)$ then $m_{i} \in(0,{1})$ and thus it on the correct side, and inside the margin 
if $\xi_{i}=1$, then $m_{i}=0$ and thus it must be on the decision boundary 
If $\xi_{i}>1$, then $m_{i}<0$ and it must be on the wrong side. 



# Proposition 
The soft margin SVM is also the unconstrained minimisation of $\frac{1}{2}\lVert \mathbf{w} \rVert^2_{2}+C \sum_{i=1}^n \ell(y_{i}(\langle \mathbf{w},\mathbf{x}_{i} \rangle + b ))$

The first term favours small weights, while the second penalises functional margins below $1$.


## The role of C
A larger $C$ will lead to a stronger emphasis on keeping margin violations low, while a smaller $C$ will lead more importance into the minimisation of the weight vector $\lVert \mathbf{w} \rVert_{2}^2$.

