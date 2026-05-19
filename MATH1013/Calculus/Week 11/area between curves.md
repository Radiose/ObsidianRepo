Net area between curves
This is an important application of [[Definite integral|integration]].
We make an important distinction between the *net* area between curves and the area between curves
# Net area between curves 
This is simple, where we just take the [[Definite integral]] over the entire domain we want. 
![[Pasted image 20260519152232.png]]
For example, finding the net area above $y = x^2$ and $y = 2x-x^2$ over the interval $[0,1.5]$ can be done simply by taking the integral $\int_{0}^{1.5}(2x-x^2)-x^2dx$

# Area between curves 
This is more complicated, where we need to take the absolute value of the difference between the two.
![[Pasted image 20260519152443.png]]
We need to take the absolute value between the two curves 
$\int_{0}^{1.5}|(2x-x^2)-x^2|dx$ 
Taking the absolute value of an integral normally is very hard. Instead we split up the domain via the following process:
1: find when the curves intersect $2x-x^2=x^2$
$\implies 2x-2x^2=0$
$\implies 2x^2-2x=0$
$2((x-1)(x+0))$
$x =1$, $x=0$
2: put each sub interval each function, and figure out what one is above the other 

3: $\int_{0} ^{1} (2x-x^2)-x^2dx$ + $\int_{1} ^{1.5} x^2-(2x-x^2)dx$
