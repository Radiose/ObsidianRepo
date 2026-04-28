---
aliases:
  - integral
  - integration
---
Definite integral 
For any function f, and any real numbers a, b such that $a<b$ and f is defined on $[a,b]$, we say that *f is integrable on \[a,b]*  if there exists a real number L with the following property: $\forall_{\epsilon} \in (0,\infty),\ \ \exists_{\delta} (0,\infty)$

such that for every partition P = $\{ x_{0},x_{1},x_{2}\dots x_{n} \}$ of $[a,b]$, and for every choice of sample points $S = (x_{1}^*,x_{2}^*\dots x_{n}^*)$ associated to P, 

$||P||<\delta \implies |R(f,P,S)-L|<\epsilon$
(the norm of the partition being less than delta implies that the absolute value of the [[Riemann sum]] minus the real number L is less than epsilon)
Or, having a small norm is a [[sufficient and necessary conditions|sufficient condition]] to force the sum close to some real number L, which we then denote as the integral of *f*. 


Because this is basically a [[limits|limit]], [[The formal definition of a limit]] is linked here.

When f is integrable on $[a,b]$, we write $\int _a^b f(x)\ dx = \lim_{ ||P|| \to 0 } \sum_{i=1}^nf(x_{i}^*)\Delta x_{i}=L$

No matter how small the difference between the [[Riemann sum]] sum and the area under the curve, there will always be a [[partition]] with small enough differences between elements such that it makes it the difference accurate enough. 


![[Sequence definition of the Definite integral]]