Binding a [[Definite integral]].

Binding a function between two numbers means finding two numbers m and n such that $m\le f(x) \le n$. 
Binding an integral involves doing the same thing, except you add the integral for f(x) over both m and n 


Start with $\int_{0}^5 x^2$
on the closed interval \[0,5], we evaluate this to find the [[Maxima and minima]] of the function.  
because f(x) is always increasing, we can skip [[The closed interval method]].

f(0) = 0, f(5) = 25

$0\le x^2\le25$

due to [[linearity]]:
$\int_{0}^50 \le\int_{0}^5x^2 \le \int_{0}^525$

$\int_{a}^b c$ = $c(b-a)$
$25(5-0)=125$
thus $0 \le \int _{0}^5x^2\le 125$

Slightly more difficult example 

$\int_{\frac{\pi}{4}}^{3\pi/4} \sin^2(x)$ 
recall that this is binding between radians of one eighth and 3 eighths of the unit circle. 
Because these are symmetrical over the y axis, the [[Maxima and minima]] of this function will be the y coordinate at each of these (the same) and the max height of the unit circle (1).

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "attachments/Ink/Drawing/2026.4.27 - 18.13pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
Now, remember that $\sin^2(x) = (\sin(x))^2, not\ \sin(x^2)$
$sin^2\left( \frac{3\pi}{4} \right)$=$\frac{\sqrt{  2}}{2}^2$ = $\frac{2}{4}=\frac{1}{2}$
thus$\frac{1}{2}\le \sin^2(x) \le 1$

thus $\int_{\frac{\pi}{4}}^{\frac{3\pi}{4}}\left( \frac{1}{2} \right)\le\int_{\frac{\pi}{4}}^{\frac{3\pi}{4}}(\sin^2(x))\le\int_{\frac{\pi}{4}}^{\frac{3\pi}{4}}(1)$
$\iff\left( \frac{1}{2}\left( \frac{3\pi}{4}-\frac{\pi}{4} \right) \right) \le \int_{\frac{\pi}{4}}^{\frac{3\pi}{4}}(\sin^2(x))\le\left( 1\left( \frac{3\pi}{4}-\frac{\pi}{4} \right) \right)$
$\iff \frac{\pi}{4} \le \int_{\frac{\pi}{4}}^{\frac{3\pi}{4}}(\sin^2(x))\le \frac{\pi}{2}$
