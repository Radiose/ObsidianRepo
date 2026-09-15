---
aliases:
  - candidate model
---
# The total idea of this note 
1: Use [[prior knowledge]] to build candidate models. 
2: estimate $E_{out}$ for each using either the singular [[validation set]] or cross validation.
3: Select the model with the least error on the validation method
4: refit on all data available, using the selected model and obtain the final $hhat$

# Choosing a model 
The total error is

$$E_{out}(\hat{h}_{n})-E_{out}(f^*)=(E_{out}(h^*)-E_{out}(f^*))+(E_{out}(\hat{h}_{N})-E_{out}(h^*))$$
The total error is equal to the [[hypothesis set|approximation error]], plus the estimation error. 

The approximation error is the price of restricting $\mathcal{H}$, and the estimation error is the price of having finite data. 
![[Pasted image 20260814094755.png]]

Above we can see the space of all hypothesis, with two candidate hypothesis sets. 
If we reduce the space, we can see that we are introducing bias. 
A smallest set gives us a smaller estimation error, but will introduce large bias. 

A larger set will give us a larger estimation error, but less bias. We need more samples. 

## The tradeoff:
![[Pasted image 20260814095027.png]]

We need some good mix between the approximation, and the estimation error.
With more data, we move the spot to the right. We can afford a more complex model. 
With something too simple, we are underfitting. 
With something too complex, $h^*$ is close to $f^*$, but we cannot find it. We are overfitting. 
![[Pasted image 20260814095251.png]]
this is an example of trying to fit some model to $\sin\left( \frac{2\pi}{x} \right)$. 
We have six independent samples, fitted in three hypothesis sets. The dots are data of one of the six samples, and the black curve is the hypothesis learned from it. 
As you can see, on the simple, the approximation error is very low, but the bias is huge. On the right, each sample is very different, so huge [[variance]], but no bias. 
The right hand is too complex, so it depends on noise too much. As complexity is increased, target is overshot and overfitting occurs. 

We want some simple [[hypothesis set]] that doesn't have a lot of variability within the samples. We also want out hypothesis set to be close to the [[target function]]. Note that a huge hypothesis set will contain something close to $f^*$, but we will not be able to use it. 


To solve this, we use our prior knowledge.


# Actual model selection

A candidate model $\mathcal{M}\subset \mathcal{H}$ is a smaller hypothesis set. We collect each model to be created via the [[prior knowledge]] we have. 

We want our models to have distinct complexities. In particular, we should have chains of models, with increasing complexities. $\mathcal{M}_{1}\subset \mathcal{M}_{2}\subset\dots \subset\mathcal{M}_{p}$, each with increasing complexities. 

## Examples

Variable selection 
![[Pasted image 20260820175701.png|620]]

### The problem with selecting off of in sample error 

If we base things off the in sample error, we will see that it will always decrease with model complexity. If we increase the space, the best hypothesis can only get better. 

If we have error with polynomial of degree 2 vs degree 3, we can only make it better. Looking at in sample error will always decrease. We need a way of selecting a model based off of $E_{out}$, computed on data that didn't play any part in the fitting. 




In order to solve this problem, we split our data set into two, before any fitting is done. 

![[validation set]]

![[test sample]]