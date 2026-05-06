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


# inverse of Cosine 
Similar to how we defined restricted sin, we restrict cosine over the interval $Cos:[0,\pi] \to [-1,1]$ to get $\arccos:[-1,1] \to [0,\pi]$, where $\arccos(x)=\theta$

Similarly to how the [[Derivative]] of arcsin was defined, we define the derivative of arccos as follows
$\frac{d}{dx}\arccos(x)=-\frac{1}{\sqrt{ 1-x^2 }}$


# Inverse of Tan 
We restrict tan on the interval $\left[- \frac{\pi}{2} , \frac{\pi}{2}\right]$, with its codomain being $\mathbb{R}$
Thus, we define $\arctan:\mathbb{R}\to\left[ -\frac{\pi}{2}, \frac{\pi}{2} \right]$ , with $\arctan(x)=\theta$

Via the inverse function theorem ,$\frac{d}{dx}\arctan(x)=\frac{1}{\sec^2(\theta)}$
Now getting it terms of x 
$\sin^2+\cos^2=1$(using [[Proof of all trigonometric identities|trig identity]]s)
$\iff \tan^2\theta+1=\sec^2(\theta)$
$\iff x^2+1=\sec^2(\theta)$
thus, $\frac{d}{dx}(\arctan(x))=\frac{1}{1+x^2}$



# Use in [[Definite integral|integration]]
The fact that the inverse trig functions have derivatives that take these forms mean that they are very useful in certain integration problems. There are two main methods:
## Direct [[Indefinite integral|antiderivative]]s

$\int \frac{1}{\sqrt{ 1-x^2 }}dx$
$\arcsin(x)+c$

$\int \frac{1}{\sqrt{ 16-9x^2 }}$ - The goal is to algebraically manipulate this to get the integrand $\frac{1}{\sqrt{  1-x^2}}$

$\int \frac{1}{16\left( 1-\frac{9}{16}x^2 \right)}$
$\frac{1}{4}\int \frac{1}{\sqrt{ 1-\frac{9x^2}{16} }}$
$\frac{1}{4} \int \frac{1}{\sqrt{ 1-\left( \frac{3x}{4} \right)^2 }}$
Using U substitution
$u = \frac{3}{4}x$
$\frac{du}{dx}=\frac{3}{4}$
$dx=\frac{4}{3}du$
$\frac{1}{4} \int \frac{1}{\sqrt{ 1-u^2 }} \frac{4}{3}du$
$\frac{1}{3} \int \frac{1}{ 1- u^2} du$
$\frac{1}{3}\arcsin(u)+c$
$\frac{1}{3}\arcsin\left( \frac{4x}{3} \right)+c$

Without a fraction 
$\int \sqrt{ 1-x^2 }$
Let $x = \sin \theta$, where $\theta \in [-\frac{\pi}{2}, \frac{\pi}{2}]$
$\frac{dx}{d\theta}=\cos(\theta)$
$\cos \theta \times d\theta=\cos(x)$
$\int \sqrt{ 1-x^2 } = \int \sqrt{ 1-\sin^2 \theta } = \int \sqrt{ \cos^2\theta }dx$
$\int \sqrt{ \cos^2\theta }\cos \theta \times d\theta$
$\int \cos^2\theta d\theta$

Oh you thought we were done?
by the trig identity $\cos^2\theta=\frac{1+\cos(2\theta)}{2}$

$\int \frac{1}{2}+ \frac{1}{2}\int \cos(2\theta)d\theta$
$\frac{1}{2}\left[ \frac{1}{2}\sin(2\theta) +\theta+c\right]$
$\frac{1}{4}\sin \theta + \frac{\theta}{2}+c$
using double angle [[Proof of all trigonometric identities|trig identity]]($\sin (2\theta)=\sin \theta \cos \theta+\sin \theta \cos \theta$)
$\frac{1}{2}\sin \theta \cos \theta+\frac{1}{2}\theta+c$



Inverse trig substitution
$\int \sqrt{ a^2-x^2 }$
$$