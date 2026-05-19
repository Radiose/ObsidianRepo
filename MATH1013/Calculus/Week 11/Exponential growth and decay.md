---
aliases:
  - exponential growth
  - exponential decay
---
Exponential growth and decay

This is a very important application of exponential functions. In many natural phenomena, quantities grow or decay at a rate proportional to their own size. This means, that if $y(t)$ is the value of such a quantity at a time $t$, then $\frac{dy}{dt}=k y$, where $k$ is the *constant of proportionality*. This is when the importance of [[Eulers number and the exponential|eulers number]] becomes very apparent. 

This is a [[Separable ODE]], so we solve it accordingly 

$\frac{dy}{dt}=ky\implies\frac{{1}}{y}dy=k \ dt$
$\implies \frac{1}{y}dy=\int kdt$
$\implies \ln|y|=kt+C$
$\implies y = e^Ce^{kt}$
$\implies y = Ae^{kt}$, where $A =e^C,-e^C, or$ 0
We note that when $t = 0$, the solution gives $y = A$, that is $y(0) = A$
Thus we write the general solution as $y = y(0)e^Ce^{kt}$

[[theorem]] from ODEs 
The only solutions of $\frac{dy}{dt}=ky$ are the exponential functions: 
$y = Ae^{kt}$ and $y = Ae^{-kt}$,