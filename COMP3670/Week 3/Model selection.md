---
aliases:
  - candidate model
---
A candidate model $\mathcal{M}\subset \mathcal{H}$ is a smaller hypothesis set. We collect each model to be created via the [[prior knowledge]] we have. 

We want our models to have distinct complexities. In particular, we should have chains of models, with increasing complexities. $\mathcal{M}_{1}\subset \mathcal{M}_{2}\subset\dots \subset\mathcal{M}_{p}$, each with increasing complexities. 

## Examples

Variable selection 
![[Pasted image 20260820175701.png|620]]

# The problem with selecting off of in sample error 

If we base things off the in sample error, we will see that it will always decrease with model complexity. If we increase the space, the best hypothesis can only get better. 

If we have error with polynomial of degree 2 vs degree 3, we can only make it better. Looking at in sample error will always decrease. We need a way of selecting a model based off of 




In order to solve this problem, we split our data set into two, before any fitting is done. 

![[validation set]]

![[test sample]]