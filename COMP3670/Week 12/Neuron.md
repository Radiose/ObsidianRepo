# Background 
The neuron is the fundamental building block in neural networks, the form of machine learning used in most modern AI systems. 

# Definition 
A single neuron is essentially just [[logistic regression]].
It computes a weighted sum of its inputs, plus a bias and applies a fixed nonlinear function to it, called the **activation**.
Logistic regression is neuron using *sigmoid* activation. Its output estimates $\eta(\mathbf{x})=\mathbb{P}(Y=1|\mathbf{X}=\mathbf{x})$ with its decision boundary the hyperplane. 

For curved boundaries, the [[SVM]] changes the boundaries, with a transformation chosen in advance. A [[neural network]] places layers of neurons between the input, and the output, and *learns* the new variables from the data.

![[Pasted image 20261031141500.png]]