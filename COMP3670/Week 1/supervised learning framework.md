# Example 
Consider the following example: 

A bank wants to automatically approve or deny credit card applications based on information about each applicant. 

Each applicant is described by some feature vector $\mathbf{x}=\{ x_{1},x_{2},\dots,x_{n} \}$
In this example, $x_{1}=$ annual income, $x_{2}=$ years employed...

The task is to learn from data to create some [[function]] that is able to predict the outcome of future applicants. 

In any supervised learning problem, we always assume there exists some *ideal rule* $f:\mathcal{X}\to \mathcal{Y}$ that best maps every input to its output. 

The target function $f$ is unknown. What we observe is a finite dataset of output input pairs that *reflect* $f$, but importantly it may have noise. 

- Measurements can be imperfect, and outcomes can be uncertain. 

![[hypothesis set]]
# The learning algorithm 

The key idea is that $\forall h \in \mathcal{H}$, we can measure the **error** of $h$.  

Some learning algorithm $\mathcal{A}$ searches through $\mathcal{H}$ and selects the hypothesis that minimises the error on the training sample. 

The selected hypothesis is denoted $\hat{h}$, that we will use as the approximation of the target function $f$.

The goal of machine learning is not to minimise error on the training sample, rather to minimise error on future, **unseen** inputs. 

The relation between these two is the central question of statistical learning theory. 