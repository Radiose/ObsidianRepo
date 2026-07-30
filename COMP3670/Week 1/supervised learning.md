This is where we observe *labelled* examples. Some data will contain some inputs and some outputs. 

### Notation 
We denote $x$ for inputs, and $y$ for labels, outcomes or outputs. When the quantity is actually a [[vector]] $(x_{1},\dots,x_{n})$ of values instead of a unique value, we denote it with boldface **x**. The set of all possible values of **x** is denoted $\mathcal{X}$ and of $y$ by $\mathcal{Y}$. The dataset is denoted by $\mathcal{D}=\{ (\mathbf{x}_{1},y_{1}),\dots,(\mathbf{x}_{n},y_{n}) \}$.

Each $\mathbf{x_{i}}$ is a feature vector, and each $y_{i}$ is the known outcome for that output. We have a dataset with $N$ examples of input and output. 

The task is to learn a new [[function]] $h: \mathcal{X} \to \mathcal{Y}$ such that $h(\mathbf{x}_{i}) \approx y_{i}$ for all $i=1\dots N$ that also works on unseen inputs (generalises).

# Forms of supervised learning

![[classification]]

![[regression]]


Some examples for each:
Spam emails - classification - $y =$ {spam, not spam} 
Image classification - $\mathbf{x}=$ pixel intensities, $y \in$ {dog, horse, cat}

Regression examples: 
House price prediction, weather forecasting, life expectancy.


# Supervised learning framework

Consider the following example: 

A bank wants to automatically approve or deny credit card applications based on information about each applicant. 
Each applicant is described by some feature vector $\mathbf{x}=\{ x_{1},x_{2},\dots,x_{n} \}$
