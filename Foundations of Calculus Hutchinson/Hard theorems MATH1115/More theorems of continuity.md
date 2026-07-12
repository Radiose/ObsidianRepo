[[theorem]]s:

1:
If $f$ is [[continuous function|continuous]] on $[a,b]$ and $f(a)<0<f(b)$, then there exists an $x \in[a,b]$ such that $f(x)=0$.
(Geometrically, this means that the graph of a [[continuous function|continuous]] function which starts below the $x$ axis and ends above it must contain a root)


2: 
If $f$ is continuous on $[a,b]$, then $f$ is bounded above on $[a,b]$, that is, there exists a some number $N$ s.t $f(x)\leq N$ for all $x \in[a,b]$
This means there is some horizontal line that lies above the graph of the function 

3: 
if $f$ is continuous on $[a,b]$, then there is some number $y$ in $[a,b]$ such that $f(y) \geq f(x)$ for all $x \in [a,b]$


# Strength of the theorems 
All theorems require continuity as a hypothesis, (theorems can be vacuously true).
Consider the function shown below 
![[Pasted image 20260706165453.png]]

The function is defined piecewise as $x \in [0,\sqrt{ 2 }) \iff f(x) = -1$ and $x \in[\sqrt{ 2 },2] \iff f(x)=1$ 
Obviously, this function is not continuous at $\sqrt{ 2 }$, but it is continuous at all other points in the interval. Additionally, it meets the requirements of theorem 1, with $f(0)<0<f(2)$, but there is no $x$ such that $f(x) = 0$.



Similarly, suppose a function $f$ exists as shown below 

![[Pasted image 20260706195408.png]]
This function is defined piecewise as $f(x)=\frac{1}{x}\iff x\not=0$ and $f(x)=0 \iff x = 0$. This function is continuous on $[0,1]$ for all points except $0$, but we can see it is not bounded. For any number $N>0$, $f\left( \frac{1}{2N} \right)=2N>N$ (because $f\left( \frac{1}{2N} \right)=\frac{1}{\frac{1}{2N}}$). 

This observation also demonstrates how theorem 2 doesn't work on open intervals.

Finally, consider the function shown below 
![[Pasted image 20260706201200.png]]
This function is defined piecewise as $f(x) = x^2 \iff x <1$ $f(x)=0 \iff x\geq 1$

On the interval $[0,1]$, $f$ is clearly bounded above, so the function $f$ does satisfy some conclusion of the second theorem, even though its not continuous on $[0,1]$. $f$ does not however, satisfy the conclusion of theorem 3, there is no $y \in[0,1]$ such that $f(y) \geq f(x)$ for all $x \in[0,1]$. This is because there are infinite reals between 0 and 1.

This conclusion shows the strength of theorem 3 being significantly greater than theorem 2. Theorem 3 is often paraphrased by saying that a continuous function on a closed interval takes its maximum value on that interval. 




## The trivial consequences built off the original 3
Theorem 4:
if $f$ is continuous on $[a,b]$ and $f(a)<c<f(b)$, then there exists an $x$ in $[a,b]$ such that $f(x) = c$
Proof:
Let $g =f-c$. Then, $g$ is continuous and $g(a)<0<g(b)$. By theorem 1, there exists an $x \in [a,b]$ such that $g(x)=0$, but this means that $f(x)=c$.

Theorem 5:
If $f$ is continuous on $[a,b]$ and $f(a)>c>f(b)$, then there is some $x$ in $[a,b]$ such that $f(x)=c$
Proof:
The function $-f$ is continuous on $[a,b]$ and $-f(a)<c< -f(b)$.
Via theorem 4, there exists an $x \in[a,b]$ such that $-f(x)=-c$, which means that $f(x)=c$

Theorem 6:
If $f$ is continuous on $[a,b]$, then $f$ is bounded below on $[a,b]$, that is, there exists some number $N$ such that $f(x) \geq N$ for all $x \in[a,b]$
Proof:
The function $-f$ is continuous on $[a,b]$, so then by theorem 2, there exists a number $M$ such that $-f(x)<M$ for all $x \in[a,b]$. But this means that $f(x) \geq -M$ for all $x \in [a,b]$, so we let $N = -M \blacksquare$


Theorem 7
If $f$ is continuous on $[a,b]$, then there is some $y \in [a,b]$ such that $f(y) ≤ f (x)$ for all $x \in [a,b]$. (A continuous function on a closed interval takes on its minimum value on that interval.) 

PROOF The function $−f$ is continuous on $[a,b]$; by Theorem 3 there is some $y$ in $[a,b]$ such that $−f (y) ≥−f (x)$ for all $x \in [a,b]$, which means that $f (y) ≤ f (x)$ for all $x$ in $[a,b]$.

## Non trivial consequences 

Theorem 8:
If $\alpha > 0$, then there exists some number $x$ such that $a = x^2$
Proof
Consider the function $f(x)=x^2$, which is certainly continuous. Notice the statement of the theorem can be expressed in terms of $f$. We can then use theorem 4.

There is obviously a number $b>0$ such that $f(b)>\alpha$. In fact, if $\alpha >1$, we can take $b = \alpha$, else we can take $b = 1$. Since $f(0)<\alpha<f(b)$, theorem 4 applied to $[0,b]$ implies that for some $x \in[0,b]$ $f(x)=\alpha$.


The same argument can be used to prove t
hat a positive number has an $n$th root, for any natural number $n$. If $n$ happens to be odd, one can do better. We can prove that any number, positive or negative, has an $n$th root. This can be done by proving that the positive number $\alpha$ has the $n$th root, then $(-x)^n=-\alpha$ since $n$ is odd. 


Theorem 9:
if $n$ is odd, then any equation $x^n+a_{n-1}x^{n-1}+\dots+a_{0}$ has a root. 

Proof: 
Consider the function $f(x)=x^n+a_{n-1}x^{n-1}+\dots+a_{0}$
We would like to prove that $f$ is sometimes positive, and sometimes negative. The idea is that for large $|x|$, the function is like $g(x)=x^n$ and since $n$ is odd, the function is positive for large positive $x$ and negative for large negative $x$. 

We rearrange $f(x)$ into $x^n(1+\frac{a_{n-1}}{x}+\frac{a_{n-2}}{x^2}\dots+\frac{a_{0}}{x^n})$
Via the triangle inequality, we get $|\frac{a_{n-1}}{x}+\frac{a_{n-2}}{x^{2}}+\dots+\frac{a_{0}}{x^n} \leq \frac{|a_{n-1}|}{|x|} + \frac{|a_{n-2}|}{|x^2|}+\dots+\frac{|a_{0}|}{|x^n|}$
Consequently, if we choose an $x$ satisfying $|x|>1,2n|a_{n-1}|,\dots,2n|a_{0}|$, 
then $|x^k|>|x|$ and 
$$\frac{|a_{n-k}|}{|x^k|} < \frac{|a_{n-k}|}{|x|} < \frac{|a_{n-k}|}{2n|a_{n-k}|} = \frac{1}{2n},$$

so, 
$$\left|\frac{a_{n-1}}{x} + \frac{a_{n-2}}{x^2} + \cdots + \frac{a_0}{x^n}\right| \leq \underbrace{\frac{1}{2n} + \cdots + \frac{1}{2n}}_{n \text{ terms}} = \frac{1}{2}.$$
In other words,

$$-\frac{1}{2} \leq \frac{a_{n-1}}{x} + \cdots + \frac{a_0}{x^n} \leq \frac{1}{2},$$

which implies that

$$\frac{1}{2} \leq 1 + \frac{a_{n-1}}{x} + \cdots + \frac{a_0}{x^n}.$$

Therefore, if we choose an $x_1 > 0$ which satisfies $|x^k|>|x|$, then

$$\frac{(x_1)^n}{2} \leq (x_1)^n \left(1 + \frac{a_{n-1}}{x_1} + \cdots + \frac{a_0}{(x_1)^n}\right) = f(x_1),$$

so that $f(x_1) > 0$. On the other hand, if $x_2 < 0$ satisfies $|x^k|>|x|$, then $(x_2)^n < 0$ and

$$\frac{(x_2)^n}{2} \geq (x_2)^n \left(1 + \frac{a_{n-1}}{x_2} + \cdots + \frac{a_0}{(x_2)^n}\right) = f(x_2),$$

so that $f(x_2) < 0$.

Now applying Theorem 1 to the interval $[x_2, x_1]$ we conclude that there is an $x$ in $[x_2, x_1]$ such that $f(x) = 0$. $\blacksquare$

Not much can be said currently regarding even degree $n$'s, at least in the current form. If we rearrange however to get $x^n + a_{n-1}x^{n-1}+\dots+a_{0}=c$, where $c$ is allowing the constant term $a_{0}$ to vary. 

The graph of a function $f(x)=x^n+a_{n-1}x^{n-1}+\dots+a_{0}$ where $n$ is even will contain a lowest point. That is, there is a number $y$ such that $f(y)\leq f(x)$ for all numbers $x$. The proof depends on theorem 7 but is tricky. The problem is making sure that the interval selected contains said $y$.

Theorem 10
if $n$ is even and $f(x) =x^n+a_{n-1}x^{n-1}+\dots+a_{0}$, then there exists a number $y$ such that $f(y)\leq f(x)$
for all $x$.

Proof:
Similarly to theorem 9, if $M = max(1,2n|a_{n-1}|,\dots,2n|a_{0}|)$
Then for all $x$ with $|x|\geq M$ we have $\frac{1}{2}\leq 1+ \frac{a_{n-1}}{x}+\dots+\frac{a_{0}}{x^n}$

Since $n$ is even, then $x^n>0$ for all $x$, so 

$$\frac{x^n}{2} \leq x^n\left(1 + \frac{a_{n-1}}{x} + \cdots + \frac{a_0}{x^n}\right) = f(x),$$

provided that $|x| \geq M$. Now consider the number $f(0)$. Let $b > 0$ be a number such that $b^n \geq 2f(0)$ and also $b > M$. Then, if $x \geq b$, we have (Figure 9)

$$f(x) \geq \frac{x^n}{2} \geq \frac{b^n}{2} \geq f(0).$$

Similarly, if $x \leq -b$, then

$$f(x) \geq \frac{x^n}{2} \geq \frac{(-b)^n}{2} = \frac{b^n}{2} \geq f(0).$$

Summarizing:

$$\text{if } x \geq b \text{ or } x \leq -b, \text{ then } f(x) \geq f(0).$$

Now apply Theorem 7 to the function $f$ on the interval $[-b, b]$. We conclude that there is a number $y$ such that

$$(1) \qquad \text{if } -b \leq x \leq b, \text{ then } f(y) \leq f(x).$$

In particular, $f(y) \leq f(0)$. Thus

$$(2) \qquad \text{if } x \leq -b \text{ or } x \geq b, \text{ then } f(x) \geq f(0) \geq f(y).$$

Combining $(1)$ and $(2)$ we see that $f(y) \leq f(x)$ for all $x$. $\blacksquare$



**Intuitively:**, we first show that for $|x|\geq b$, $f(x)\geq f(0)$. or that for all $x\not \in[-b,b]$ we will have $f(x)\geq f(0)$.

We then apply theorem 7 to $f$ in that interval $[-b,b]$, getting the minimum $y \in[-b,b]$ with $f(y)\leq f(x)$ for all $x \in[-b,b]$.

Additionally, we must $f(0)$ in that interval logically, so for any $x$ outside $[-b,b]$, $f(x)\geq f(0)\geq f(y)$


Theorem 11:
Consider the equation $$(*)\ \ \ x^n+a_{n-1}x^{n-1}+\dots+a_{0}=c$$
and suppose $n$ is even. Then there exists a number $m$ such that $(*)$ has a solution for $c \geq m$ and has no solution for $c <m$ 


Let $f(x) = x^n +a_{n-1}x^{n-1}+\dots+a_{0}$
According to theorem 10, there is a number $y$ such that $f(y)\leq f(x)$ for all $x$.
Let $m=f(y)$. If $c<m$, then the equation $(*)$ obviously has no solution. If $c =m$, then $(*)$ has $y$ as a solution. Finally suppose $c > m$. Then, let $b$ be a number such that $b > y$ and $f(b)>c$. Then, $f(y)= m < c <f(b)$. By theorem 4, there is some number $x$ in $[y,b]$ such that $f(x)=c$, so $x$ is a solution of $(*) \blacksquare$.


Proving theorems 1,2 and 3 require the [[Completeness axiom]], because we require knowing that the reals have no gaps in them, which is further elaborated on in the [[Density of the rational and irrational numbers]] note.

## Trying to prove theorem 1 without the completeness axiom: 

Let us attempt to prove theorem 1 by locating the smallest $x \in[a,b]$ such that $f(x)=0$. 
Consider the set $A = \{ x \in[a,b]|f(t)<0 \text{ for all }t \in[a,x] \}$. We visualise this below. 
![[Pasted image 20260709103225.png]]
$A$ is marked above by the heavy line, $x$ in the diagram is in A, while $x'$ is not. 
Since $f$ is negative at $a$, and positive at $b$, then the set $A$ itself contains some points greater than $a$. All points sufficiently close to $b$ are not in $A$. Now suppose $\alpha$ is the smallest number which is greater than all members of $A$ (least upper bound). We claim that $f(\alpha)=0$. To prove this we simply eliminate the possibilities $f(\alpha)>0$ and $f(\alpha)<0$. 

Suppose first that $f(\alpha)<0$. Then by theorem 6-3, $f(x)$ would be less than 0 for all $x$ in a small interval containing $\alpha$, in particular for some numbers bigger than $\alpha$. But this contradicts the fact that $\alpha$ is bigger than every member of $A$ (particularly larger numbers than $\alpha$). Thus, $f(\alpha)\not<0$.

Now we deal with the $f(\alpha)>0$ case. Again, applying theorem 6-3, we see that $f(x)$ would be positive for for all $x$ in a small interval around $\alpha$, particularly those less than $\alpha$, which implies that these numbers are not in $A$. Thus, $\alpha$ cannot be the *least* upper bound. Thus, $f(\alpha)=0$. We are tempted to say $\blacksquare$.

However, this proof is missing an important part. This proof assumes that there exists a number $\alpha$ that is the smallest number which is greater than all members of $A$. We have no way of knowing whether this is actually possible without the completeness axiom. 


# Proving with the axiom 
We define the set $A$ as follows:
$A = \{ x : a \le x \le b, \text{ and }f\text{ is negative on the interval }[a,x] \}$
![[Pasted image 20260712185730.png]]
Clearly, $A \not= \emptyset$, since $a$ is in $A$; in fact, there is some $\delta > 0$ such that $A$ contains all points $x$ satisfying $a\le x < a+\delta$. This follows since $f$ is [[continuous function|continuous]] on $[a,b]$ and $f(a)<0$. Similarly, $b$ is an upper bound for $A$, and there is a $\delta>0$ such that all points $x$ satisfying $b-\delta<x\le b$ are upper bounds for $A$. 

From these remarks, it follows that A has a [[Completeness axiom|supremum]] $\alpha$ and that $a<\alpha<b$. 
We wish to show that $f(\alpha)=0$ via eliminating possibilities $f(\alpha)<0$ and $f(\alpha)>0$. 



Suppose first that $f(\alpha) < 0$. By Theorem 6, there is a $\delta > 0$ such that $f(x) < 0$ for $\alpha - \delta < x < \alpha + \delta$ (Figure 2). Now there is some number $x_0$ in $A$ which satisfies $\alpha - \delta < x_0 < \alpha$ (because otherwise $\alpha$ would not be the *least* upper bound of $A$). This means that $f$ is negative on the whole interval $[a, x_0]$. But if $x_1$ is a number between $\alpha$ and $\alpha + \delta$, then $f$ is also negative on the whole interval $[x_0, x_1]$. Therefore $f$ is negative on the interval $[a, x_1]$, so $x_1$ is in $A$. But this contradicts the fact that $\alpha$ is an upper bound for $A$; our original assumption that $f(\alpha) < 0$ must be false. 


Suppose, on the other hand, that $f(\alpha) > 0$. Then there is a number $\delta > 0$ such that $f(x) > 0$ for $\alpha - \delta < x < \alpha + \delta$.
Once again we know that there is an $x_0$ in $A$ satisfying $\alpha - \delta < x_0 < \alpha$; but this means that $f$ is negative on $[a, x_0]$, which is impossible, since $f(x_0) > 0$. Thus the assumption $f(\alpha) > 0$ also leads to a contradiction, leaving $f(\alpha) = 0$ as the only possible alternative.