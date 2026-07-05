---
aliases:
  - continuous
---
continuous functions 

let f be a function and let $a\in \mathbb{R}$
We say that f is continuous at a if 
the domain of f includes some neighbourhood of a $N(a,\delta)=(a-\delta,a+\delta) \subset domain(f)$ for some $\delta>0$
The limit exists ($\lim_{ x \to a^- }f(x)=\lim_{ x \to a^+ }f(x)$)
The limit exists as x approaches a 
$\lim_{ x \to a }f(x)$=f(a) 
All of these are important.


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "attachments/Ink/Drawing/2026.3.3 - 10.40am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
![[continuous on an interval]]


you can use continuity with limit laws. IE by proving f(x) = x is continuous at a, you can prove that x^2 at a is continuous, as the product of two [[continuous function]] is also continuous. 

Suppose that g(x) is continuous. and that lim f(x) exists and belongs to the domain of g
then $\lim_{ x \to a }g(f(x)) = g(\lim_{ x \to a }f(x))$
eg
```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "attachments/Ink/Drawing/2026.3.10 - 9.17am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
Remember that: sin/cos are continuous at every point. A polynomial is continuous at every point. Ln(x) is continuous at positive numbers 
therefore, to compute $\lim_{ x \to a }f(x)$  it is enough to show that f is continuous at a, therefore f(a).


for example:
$\lim_{ x \to 3 } \frac {(\cos^2(3))} {x-1}$ is continuous around 3, therefore you can just plug it in

for a piecewise function:

compute the limit when x approaches from the left, and when x approaches from the right. Therefore, the function will be continuous at a if and only if the left hand limit equals the right hand limit. 





![[Theorems for continuouness]]