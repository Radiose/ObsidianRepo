---
aliases:
  - converges
  - converge
tags:
  - spivak
---
The most fundamental concept in the study of sequence is the notion of a convergence in a sequence .

The informal idea is that a [[sequence]] $a_{n}$ converges to $a$ and we write $lim \ a_{n} = a$ if no matter how small a positive number is chosen, the distance between $a_{n}$ and $a$ will always be less than this positive number for some $n$. The smaller the number, the larger $n$ will need to be.

This is an essential application of the [[limits|limit]].

It is essential to note that this must be satisfied be *any* positive number. IE, for any epsilon you choose (as small as you want),  an $n$ exists such that $|a_{n}-a| < \epsilon$

# Formal def: 
We say that the sequence $(a_{n})$ converges to $L$ and write   
$\lim_{ n \to \infty } a_{n} = a$
or $a_{n} \xrightarrow[n \to \infty]{}L$
when $\forall \epsilon>0 \exists \ \ N \in \mathbb{N}$ s.t $\forall n\geq N \ \ \  |a_{n}-L|<\epsilon$



### For example:
Show that the sequence [[Explicit definition of a Sequence|explicitely defined]] by $a_{n} = 1+\frac{1}{n^2}$ converges to 1 according to the definition 

Let $\epsilon > 0$. 

Via the definition, we have $|a_{n}-1| = \frac{1}{n^2}$
Since $\frac{1}{n^2}<\epsilon$ if $n^2 > \frac{1}{\epsilon}$, 
IE, if $n > \frac{1}{\sqrt{ \epsilon }}$, we take $N = \left[ \frac{1}{\sqrt{ \epsilon }} \right]$ or any large integer, where \[] denotes the integer part. 
This proof hinges upon the [[archimedean property]] strongly, being that there will exist a natural number N that is greater than the real number $\frac{1}{\sqrt{ \epsilon }}$

Another example:

Demonstrate that the sequence [[implicit definition of a sequence|implicitely defined]] by $a_{1}=1$ and $a_{n+1} = \frac{1}{2}a_{n}+2$ for $n \ge 1$. We calculate the first few terms and assume that the [[sequence]] converges to 4. 

We have a formula of $a_{n+1}$ in terms of $a_{n}$, so we want a formula of $|a_{n+1}-4|$ in terms of $|a_{n}-4|$
$|a_{n+1}-4| = | \frac{1}{2}n+2-4|=\frac{1}{2}|a_{n}-4|$
Thus, $|a_{1}-4|=3,$ $|a_{2}-4|=\frac{3}{2}$, $|a_{3}-4| = \frac{3}{2}^2$
In general, $|a_{n+1}-4|$$=\frac{3}{2^{n-1}}$

It follows that $|a_{n}-4|<\epsilon$ for all $n$ such that $\frac{3}{2^n-1}<\epsilon$

# Convergence axiom 
