---
aliases:
  - converges
---
The most fundamental concept in the study of sequence is the notion of a convergence in a sequence .

The informal idea is that a [[Sequence]] $a_{n}$ converges to $a$ and we write $lim \ a_{n} = a$ if no matter how small a positive number is chosen, the distance between $a_{n}$ and $a$ will always be less than this positive number. The smaller the number, the larger $n$ will need to be.

This is an essential application of the [[limits|limit]].

It is essential to note that this must be satisfied be *any* positive number. IE, for any epsilon you choose (as small as you want),  an $n$ exists such that $|a_{n}-a| < \epsilon$

Formal def: 
We say that the sequence $(a_{n})$ converges to $a$ and write   
$\lim_{ n \to \infty } a_{n} = a$
when $\forall \epsilon>0 \exists N \in \mathbb{Z}$ s.t $n>N \implies |a_{n}-a|<\epsilon$


For example:
Show that the sequence [[Explicit definition of a Sequence|explicitely defined]] by $a_{n} = 1+\frac{1}{n^2}$ converges to 1 according to the definition 

Let $\epsilon > 0$. 

Via the definition, we have $|a_{n}-1| = \frac{1}{n^2}$
Since $\frac{1}{n^2}<\epsilon$ if $n^2 > \frac{1}{\epsilon}$, 
IE, if $n > \frac{1}{\sqrt{ \epsilon }}$, we take $N = \left[ \frac{1}{\sqrt{ \epsilon }} \right]$ or any large integer, where \[] denotes the integer part. 
This proof hinges upon the [[archimedean property]] strongly. There is 