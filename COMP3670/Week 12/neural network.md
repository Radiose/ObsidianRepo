---
aliases:
  - neuron
---
![[Neuron]]

# Fully connected deep neural networks 
![[Pasted image 20261031141802.png]]

Here we have a fully connected, deep neural network. 
Every blue circle shown is a weighted sum of **all** outputs in the previous layer, plus some bias and an activation $\sigma$. This gives it the name *fully connected*.

We have $k=2$ hidden layers of width $4$. The depth is $4$, (input, output + hidden layers).
Information only flows from left to right. Our network is *feed forward*.

Our output is a score $f_{\mathbf{w}}(\mathbf{x})$ that gets converted into our distribution $\hat{\eta}(\mathbf{x})$ by the [[logistic regression]]


# ![[activation function]]

# In matrix notation 
We can represent a neural network in the form of matrices. 
Write down the weights of layer $i$ as a matrix $A_{i}$, where $(A_{i})_{i,j}=w_{I,j}^{(i)}$. Then, the network shown above can be represented as $f_{\mathbf{w}}(\mathbf{x})=A_{3}(\sigma(A_{2}\sigma(A_{1}\mathbf{x})))$, where $\sigma$ is the activation. 

In general $f_{\mathbf{w}}(\mathbf{x})=A_{k+1}\sigma(A_{k}\dots\sigma(A_{1}\mathbf{x})))$ with $A_{i}$ of size $d_{i}\times d_{i-1}$
The weights $\mathbf{w}$ are the entries of all matrices. 

# The output layer 
In [[regression]], the output $f_{\mathbf{w}}(\mathbf{x})$ is the prediction itself. In classification, the network must output probabilities, so that the last layer is followed by an activation function. 

### For 2 classes 
We've already seen this, $\hat{\eta}(\mathbf{x})$ is used with the $\mathbb{1}$ function to create $\hat{h}(\mathbf{x})$. This is in [[cross entropy loss]].

The last layer has $K$ outputs $f_{\mathbf{w},1}(\mathbf{x}),\dots,f_{\mathbf{w},k}(\mathbf{x})$ and **softmax** turns them into $K$ positive probabilities that add up to $1$.

$\hat{p}_{\mathbf{w},k}(\mathbf{x})= \frac{e^{f_{\mathbf{w},k}(\mathbf{x})}}{\sum_{j=1}^k e^{f_{\mathbf{w},j}(\mathbf{x})}}$ with $\hat{h}(\mathbf{x})=arg \max_{k}\hat{p}_{\mathbf{w},k}(\mathbf{x})$
With no hidden layers and two classes, this is just exactly [[logistic regression]]

# Universal approximation of neural networks
![[Universal approximation of neural networks]]

# Training a neural network for classification 
We have labelled training data $(\mathbf{X}_{1},Y_{1}),\dots,(\mathbf{X}_{n},Y_{n})$ with $Y_{i}\in \{ 0,1 \}$

We use empirical [[cross entropy loss]], $$J(\mathbf{w})= -\frac{1}{N} \sum_{i}[\log \hat{\eta}_{\mathbf{w}}(\mathbf{X}_{i})+(1-Y_{i})\log(1-\hat{\eta}_{\mathbf{w}}(\mathbf{X}_{i}))]$$
With $K$ classes, it becomes $J(\mathbf{w})=-\frac{1}{N} \sum_{i}\log \hat{p}_{\mathbf{w},Y_{i}}(\mathbf{X}_{i})$ minus the probability given to the correct class. 
We run [[Empirical risk minimisation]] by aiming to minimise $J(\mathbf{w})$ subject to $\mathbf{w}\in \mathbb{R}^p$ ($p$ is # of params)
This is a non [[convex function]] [[COMP3670/Week 12/optimisation|optimisation]] problem, with *multiple* local minima. 

# Risks of overfitting
For small samples, a moderately wide and deep [[neural network#Fully connected deep neural networks|FCDNN]] may overfit training data. 
We can however, regularise complexity, similar to how was done in [[Ridge regression]],  with the goal of minimising $J(\mathbf{w})+\lambda \lVert \mathbf{w} \rVert^2$

## NN example: the exclusive or 
![[Pasted image 20261031152710.png]]

One single [[The perceptron|perceptron]] cannot learn separate this, but a neural network consisting of two neurons in a single hidden layer can. 


# Gradient descent on neural networks 
One common approach to minimising $J(\mathbf{w})$ is gradient descent. 
The gradient is computed by the [[Chain rule]] applied layer by layer backwards. This is called **backpropagation**

# Initialisation 
Neural networks are typically trained with variants of [[Stochastic gradient descent]], so properly choosing the initial $\mathbf{w}(0)$ is ultra important to finding a good local minima. 
We typically use a heuristic approach, where each weight is initialised by sampling from some non zero mean uniform, or gaussian distribution.

Remember that for distributions, $\sigma$, or the [[variance]] is essential.
For weights connecting a layer $d_{i}$ of neurons to the next $d_{i+1}$ layer, they have variance scaled as a function of $d_{i}+d_{i+1}$
There are many types of variants 
- LeCun -$\sigma=\frac{1}{d_{i}}$
- He - $\sigma=\frac{2}{d_{i}}$

## Modifications to gradient descent 
Because loss distributions often have multiple local minima, and are certainly not convex, we need to adapt gradient descent principles to get the best loss.


### The heavy ball method 
The heavy ball introduces momentum into gradient descent.
Intuitively, *the heavy ball does not bounce so much off of walls, and also rolls faster on flat surfaces* 
The heavy ball update is $$\mathbf{m}(t)=\beta \mathbf{m}(t-1)-\alpha \nabla J(\mathbf{w}(t)) \\ \\ \mathbf{w}(t+1)=\mathbf{w}(t)+\mathbf{m}(t)$$
where $\mathbf{m}$ is the momentum vector, with $\mathbf{m}(0)=0$ and $\beta \in[0,1]$ is an [[Exponential growth and decay|exponential decay]] parameter. 
$\beta$=0.9 is a common choice.

### Nesterov accelerated gradient 
The nesterov method is a slight modification to the heavy ball method that usually accelerates convergence by computing the [[gradient]] not at the current value of $\mathbf{w}$, but a future version of it. 

Intuitively, a gradient closer to the minima is desirable, as it should point more strongly towards said minima. 

The update is $$\begin{aligned}
\mathbf{m}(t) &= \beta\, \mathbf{m}(t-1) - \alpha \nabla J\big(\mathbf{w}(t) + \beta\, \mathbf{m}(t-1)\big) \\
\mathbf{w}(t+1) &= \mathbf{w}(t) + \mathbf{m}(t)
\end{aligned}$$
Again, $\beta=0.9$ is commonly used.

### Adaptive gradient descent (adagrad)
This is a method to adjust learning rates of each coordinate. 

Intuitively, a smaller learning rate along directions of steepest descent is desirable, while a larger in smaller gradient directions is also useful.

The update is $$
\begin{aligned}
\mathbf{s}(t) &= \mathbf{s}(t-1) + \big(\nabla J(\mathbf{w}(t))\big)^2 \\
\mathbf{w}(t+1) &= \mathbf{w}(t) - \frac{\alpha}{\sqrt{\mathbf{s}(t)+\epsilon}}\, \nabla J(\mathbf{w}(t))
\end{aligned}$$
With $\mathbf{s}(0)=0$ and $\epsilon$ is a small number to avoid division by 0.

### RMSProp 
This is a popular variant of [[neural network#Adaptive gradient descent (adagrad)|adagrad]], where [[Exponential growth and decay|exponential decay]] is used to effectively forget older gradients. 
The update is as follws
$$
\begin{aligned}
\mathbf{s}(t) &= \beta\, \mathbf{s}(t-1) + (1-\beta)\big(\nabla J(\mathbf{w}(t))\big)^2 \\
\mathbf{w}(t+1) &= \mathbf{w}(t) - \frac{\alpha}{\sqrt{\mathbf{s}(t)+\epsilon}}\, \nabla J(\mathbf{w}(t))
\end{aligned}$$
Where $\beta$ is the exponential decay parameter between 0 and 1. Usually 0.9.

### Adaptive moment estimation (Adam optimiser)
Adam is a hybrid between momentum based and Adagrad classes of methods. 
The update is $$\begin{aligned}
\mathbf{m}(t) &= \beta_1\, \mathbf{m}(t-1) - (1-\beta_1)\, \nabla J\big(\mathbf{w}(t)\big) \\
\mathbf{s}(t) &= \beta_2\, \mathbf{s}(t-1) + (1-\beta_2)\big(\nabla J(\mathbf{w}(t))\big)^2 \\
\widehat{\mathbf{m}}(t) &= \mathbf{m}(t)/(1-\beta_1^t) \\
\widehat{\mathbf{s}}(t) &= \mathbf{s}(t)/(1-\beta_2^t) \\
\mathbf{w}(t+1) &= \mathbf{w}(t) + \frac{\alpha}{\sqrt{\widehat{\mathbf{s}}(t)+\epsilon_{\mathrm{root}}}+\epsilon}\, \widehat{\mathbf{m}}(t)
\end{aligned}$$Here $\beta_{i}$ is $\in [0,1]$ and $i=1,2$ and $\epsilon_{root},\epsilon$ are small numbers. 
Default, $\beta_{1}=0.9$, $\beta_{2}=0.999$, $\epsilon=10^{-8}$ and $\epsilon_{root}=0$
Adam is the default optimiser used for training neural networks. 