---
aliases:
  - root of unity
---
These are a property of [[Complex number|complex]] solutions to $z^n=1$
if $z^n=1$ and $z \in \mathbb{C}$, then z is called an nth root of unity

Some logic 
$z^n =1 \implies |z|^n=1 \implies |z|=0 \implies z = cis\theta$
$\implies z^n = cis(\theta) ^n = cis(n\theta)=1$
$n\theta \equiv 0 (mod 2\pi)$ - is in [[congruence modulo]]
$\implies \theta =0, \frac{2\pi}{n}, \frac{4\pi}{n}\dots, \frac{2(n-1)\pi}{n}$


The following result is via de moivres theorem: $\text{cis}(\theta)^n=\text{cis n}\theta$

the $n$th roots of $R \text{ cis}(\alpha)$ are $z_{k}=\sqrt[n]{R  }\text{\ cis}\left(\frac{\alpha+2k\pi}{n} \right)$ for $k=0,1,\dots n-1$


so the unit circle will be evenly divided by n subdivisions. 

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "attachments/Ink/Drawing/2026.5.25 - 14.51pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
this is for n = 8



## Utilising this for any polynomial 
Its important to note that this roots of unity concept can be more broadly applied to any complex solution set of a polynomial. Once you have determine one solution for the polynomial, you can utilise the logic for $z^n = 1$ to solve for a polynomial $z^n \not=1$ and find the other n-1 solutions.

If $z_{0}$ is a solution to $z^n \not=1$, then $z_{0} \cdot w_{k}$ is also a solution for any root of unity $w_{k}$
So, if you have one solution, just multiply it by $cis\left( \frac{2\pi k}{n} \right)$
