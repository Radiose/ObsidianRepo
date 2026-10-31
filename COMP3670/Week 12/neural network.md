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
