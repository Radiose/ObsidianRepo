---
{}
---
Optimisation 
You can use the tools laid out previously to find out optimal solutions to problems. If [[The closed interval method]] is not able to be used, then you should utilise [[Maxima and minima|maxima or minima]] and reason about the shape of the graph to find the optimal solution. 


Steps are: 
Get the overall relation between desired quantity and other factors (volume = formula, heat  = formula etc)

Write out the [[Function]] in terms of a singular variable 
	do this via finding some relationship. It could be described in 
Then find local [[Maxima and minima|maxima or minima]] to find what you are looking for, using [[The first Derivative test]] and [[The Second Derivative test]]





$V = \pi r^2h=1000$
to minimise the cost of the metal, find the minimal surface area 
$A = 2\pi r^2 = 2\pi rh$
(area of two ends of a can and area of sides)
Job is to minimise A
First write A in terms of R (easier than H)
$A = 2\pi r^2 = 2\pi rh$ therefore $A = 2\pi r^2+2\pi r\left( \frac{1000}{\pi r^2} \right)$
$A = 2\pi r^2 + 2 \frac{1000}{r}$
We cannot use the simple [[The closed interval method|closed interval method]], as $r \in (0,\infty)$ so its an open interval.
Computing the [[Derivative]] of A gives $A'(r) = 4\pi r- \frac{2000}{r^2}$
Solving for 0 gives an r of $(\frac{500}{\pi})^{1/3}$


