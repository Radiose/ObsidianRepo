Inverse trigonometric function
All of the typical trigonometric [[function]]s have [[Inverse function]]s as well. 
# Inverse of Sin
The typical sin function is [[continuous function|continuous]], but fails the test for being [[Injective Function|injective]]. 

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "attachments/Ink/Drawing/2026.5.6 - 10.32am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
However, by restricting the domain to $\left[ -\frac{\pi}{2}, \frac{\pi}{2} \right]$, we will get an [[Injective Function|injective]] function. Additionally, this will also lead to [[Bijective|bijection]], as the codomain will be restricted to $[-1,1]$.
Thus, we define the inverse function $\sin^{-1}(x)=\theta$ to be $\arcsin(x)=\theta$
Using the established properties of [[Inverse function]]s, we define the [[Derivative]] to be 
$\frac{d}{dx}\arcsin(x)=\frac{1}{\cos(\arcsin(x))}$
Now recall that $\arcsin(x)=\theta$, thus 
$\frac{d}{dx}\arcsin(x)=\frac{1}{\cos(\theta)}$
Using the [[Proof of all trigonometric identities|trig identity]] $\sin^2(\theta)+\cos^2(\theta)=1$, $\cos(\theta)=\sqrt{ 1-\sin^2(\theta) }$
$\cos(\theta)=\frac{1}{\sqrt{ 1-x^2 }}$ (because $\sin(\theta)=x$)


Cos