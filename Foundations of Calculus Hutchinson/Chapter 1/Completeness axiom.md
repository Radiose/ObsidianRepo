---
aliases:
  - least upper bound
---
# Statement
If A is any set of real numbers having at least one number in it, and if there exists a real number y s.t $\forall x\in A\ \ \ \ x \le y$, (we denote y the *upper bound*) then there exists a smallest such number, called the *least upper bound*, or *supremum* of A.


OR:
If *A* is a set of real numbers and $x$ is a real number such that $a ≤ x$ for every $a ∈ A$, then $x$ is called an upper bound for $A$. If in addition $x ≤ b$ for every upper bound $b$, then $x$ is called the least upper bound or supremum of $A$. In this case one writes
$x$ = lub $A$ or $x$ = sup $A$

If $x ≤ a$ for every $a ∈ A$, then $x$ is called a lower bound for $A$. If also $x ≥ c$ for every lower bound $c$, then $x$ is called the greatest lower bound or infimum of $A$. In this case one write $x =$ glb $A$ or $x$ = inf $A$. Thus we have:

#### Axiom 14: If a non empty [[set]] A has an upper bound, it has a least upper bound 

We can directly derive a similar answer of the greatest lower bound using the axiom. 
We consider the set $A^* :=\{ -x:x \in A \}$, which is obtained by reflecting the set $A$ about 0.
![[Pasted image 20260620162921.png]]

As you can see in the image above, a least upper bound of A implies a greatest lower bound of $A^*$ and vice versa. 


## Interpretation of the completeness axiom 

The main consequence of this axiom is that the implication that the [[real number]]s have no gaps in them. 

For example, the rational numbers are not a model of the axiom if, in the statement of the axiom, we replace occurrences of the word *real* with *rational*
To demonstrate, let $$A = \{ a \in \mathbb{Q}\  | \ 0 \le a \text{ and }a^2 \le 2\} = \{ a \in \mathbb{Q}\ |\ 0 \le a \le \sqrt{ 2 } \}$$
The first definition of A has the advantage of it not being defined in terms of the irrational number $\sqrt{ 2 }$. There are certainly rational numbers $x$ which are upper bounds of $A$, but we claim that *there is no rational number b which is a least upper bound of A*

Proof
We note firstly the [[Density of the rational and irrational numbers]]
Since $\sqrt{ 2 }$ is not rational, it cannot be the required $b$

On the other hand, if $b < \sqrt{ 2 }$, since there is always a rational number between b and $\sqrt{ 2 }$, then this gives a member of A between $b$ and $\sqrt{ 2 }$
If $b >\sqrt{ 2 }$, then there always exists a rational number between b and $\sqrt{ 2 }$ that is less that b, thus b cannot be the lowest bound. 

We have ruled out the three possibilities $b = √ 2, b < √ 2 \text{  and b } > √ 2$. This completes the proof of the claim. Hence there is no rational number which is a least upper bound for $A$.

