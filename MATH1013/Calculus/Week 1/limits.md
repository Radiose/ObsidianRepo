---
aliases:
  - limit
---
limits 
A function may or not be defined at a particular point, but it can have a limiting value at that point. 
for example 
$f(x) = \frac{x^3-2x+1}{x-1}$, which is a function that is defined for all real numbers except for 1. 

f(x) is not defined at x = 1 (1-1 = 0 and you cannot divide by 0), but f(0.99) = 0.97, f(0.999)  =0.997 etc
Essentially, as x gets closer and closer to 1, f(x) gets closer and closer to 1

The domain of f(x) is all numbers except 1. 
so domain f = $(-\infty,1] \cup[1,\infty)$
As x approaches 1, f(x) approaches 1. 



```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "attachments/Ink/Drawing/2026.2.26 - 17.48pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
Definition of [[limits]]

for the limit of f(x) to have any possibility of being defined at point x = a, f(x) needs to be defined for x in a *neighbourhood* of a.

A neighbourhood of a are points that are close to a, but are not a. 

$N(a,\delta):=\{ x \in \mathbb{R}$ such that $x \not= a$ but $|x-a|< \delta\}$

algebraically: 
|x-a| < $\delta$ = $\delta<x-a<\delta$=$a-\delta<x<a+\delta$ = $x \in (a-\delta,a+d)$
The smaller delta is, the closer x is to a. 

The first condition of limits:
There exists some number such that f is defined in a $\delta$-neighbourhood of a. Mathematically:
$N(a,\delta) = (a-\delta,a)\cup(a,a+\delta) \subset Domain(f)$ for some $\delta>0$

The second condition for the existence of the limit of f(x) at x=a is that points x which are close to a, should have f(x) close to some number $L_{a}\in \mathbb{R}$
In mathematical terms, this is defined as:
There exists a number $L_{a}\in \mathbb{R}$ such that for every number $\epsilon \in (0,\infty)$, there exists a number $\delta_{\epsilon}\in(0,\infty)$ such that
if $x \in N(a,\delta_{e})$ then $|f(x)-L_{a}|<\epsilon$

The point $L_{a}$ will be then defined as the limit value of f(x) as x gets close to a, or mathematically,
$\lim_{ x \to a } f(x) := L_{a}$


![[The formal definition of a limit]]

 ![[Evaluating limits using the definition]]

When limits do not exist
$\lim_{ x \to 0 }\sin\left( \frac{1}{x} \right)$ does not exist
suppose $\epsilon = \frac{1}{2}$As x gets closer and closer to 0, the value of sin(1/x) oscillates between -1 and 1 more freqently
Now matter how small the neighbourhood is, it will always contain x values such that sin(1/x) = either -1 or 1. Therefore, whatever real number L we may choose, it cannot be within $\epsilon$=1/2 of both 1 and -1.





Some ways of computing [[limits]]
a limit only depends on the values of f(x) for x in neighbourhoods of a, but not on the value of the function in x=a (it can even be undefined)
Therefore, if f(x) = g(x) for x in a neighbourhood of a, then they have the same limit as x approaches a: $\lim_{ x \to a }f(x) = \lim_{ x \to a }g(x)$


Let f,g : $\mathbb{R} \to \mathbb{R}$ be two functions and fix $a \in \mathbb{R}$ If there exists a $\delta>0$ such that 
$N(a,\delta) \subset Domain(f)$ and $N(a,\delta) \subset Domain(g)$; and 
f(x) = g(x) for all $x \in N(a,\delta)$
then $\lim_{ x \to a }f(x) = \lim_{ x \to a }g(x)$

for example: 
$\lim_{ x \to 1}\frac{(x^2-1)}{x-1}$=$\frac{(x+1)(x-1)}{x-1}$=x+1

one sided [[limits]]



Certain limits may be only approached from one side, whether that be from below or above.
![[Pasted image 20260226212227.png]]

g(x) (blue) above is one sided

Mathematically, these neighbourhoods be defined as 
from the left- $N^-(a,\delta) = (x\in \mathbb{R})$ such that $x \not= a$ but $-\delta<x-a<0=(a-\delta,a)$
From the right - $N^+(a,\delta)={x\in \mathbb{R}}$ such that $x \not= a$ but $0<x-a<\delta=(a,a+\delta)$

Definition from below 
1: there exists $\delta \in (0,\infty)$ such that $(a-\delta,a)$ is a subset of the domain of f(x)
2:for every $\epsilon \in (0,\infty)$, there exists $\delta_{\epsilon}$ > 0 such that $-\delta_{\epsilon}<x-a<0$ and $x \not= a \implies |f(x)-L_{a}|<\epsilon$ If no such $L_{a}^-$ exists, we say that the limit does not exist

Definition from above 
1: there exists $\delta \in (0,\infty)$ such that $(a,a + \delta)$ is a subset of the domain of f(x)
2:for every $\epsilon \in (0,\infty)$, there exists $\delta_{\epsilon}$ > 0 such that $0<x-a<\delta_{\epsilon}$ and $x \not= a \implies |f(x)-L_{a}|<\epsilon$ If no such $L_{a}^+$ exists, we say that the limit does not exist.

COME BACK AND FINISH TOMORROW REMARKS ABOUT ONE SIDED LIMITS