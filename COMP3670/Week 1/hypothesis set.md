---
aliases:
  - approximation error
---
via the first step of [[inductive reasoning]], we must conceive some hypothesis that we could choose after analysis of some data. 

In this credit approval, our hypothesis $h$ is some function that reads the features and outputs some decision. $h:\mathcal{X}\to \{ +1,-1 \}$.

The hypothesis [[set]] $\mathcal{H}$ is the collection of all such candidate functions we are *willing to consider* before seeing any data. We must be careful here, if we make it just the set of all functions, then we can easily overfit some model to just be defined piecewise solely on the training data. 

 Some candidate hypothesis for the example: Approve if income > 40,000, if income is high and debt is low etc. 

An important distinction is that **all** supervised learning methods contain some underlying hypothesis set, even if in practice we don't care much about it.

# Selecting the hypothesis set 
This is a very crucial decision that must be made before any learning begins. 
$\mathcal{H}$ may encode our prior knowledge about the likely form of $f$. But unfortunately, it is possible for $\mathcal{H}$ to not contain some function close to $f$. This limitation is called the **approximation error**.

However, if $\mathcal{H}$ is too complex, then it becomes easy to fit any training data, including noise. This will create some unfalsifiable model. Fitting training data perfectly to some function may not tell us anything useful, especially if the process is likely to have some form of **randomness**. This is the seed of **overfitting**.
