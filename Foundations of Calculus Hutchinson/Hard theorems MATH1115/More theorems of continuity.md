[[theorem]] 1: If $f$ is [[continuous function|continuous]] on $[a,b]$ and $f(a)<0<f(b)$, then there exists an $x \in[a,b]$ such that $f(x)=0$.
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




## More theorems built off the original 3
Theorem 4:
if $f$ is continuous on $[a,b]$ and $f(a)<c<f(b)$, then there exists an $x$ in $[a,b]$ such that $f(x) = c$
Proof:
Let $g =f-c$. Then, $g$ is continuous and $g(a)<0<g(b)$. By theorem 1, there exists an $x \in [a,b]$ such that $g(x)=0$, but this means that $f(x)=c$.

Theorem 5:
If $f$ is continuous on $[a,b]$ and $f(a)>c>f(b)$, then there is some $x$ in $[a,b]$ such that $f(x)=c$
Proof:
The function $-f$ is continuous on $[a,b]$ and 
