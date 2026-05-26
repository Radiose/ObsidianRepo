volumes of shapes via integration

Via [[The fundamental theorem of calculus]], getting the volume of a shape can be done via [[Definite integral|integration]]. This is because you can track the net change in base shape over an interval.

This is similar in process to [[Optimisation]] via differentiation.
This process is based of regular geometry. You can obtain the area of a shape by multiplying the bases area by the height. However, when shapes are irregular, and the base is constantly changing, we need to use integration. 

If we move along an X-axis, we keep in mind that we need to take a cross section thats perpendicular to X, and if we move along Y, we do the same for perpendicular to y

# Getting the volume of a sphere 


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "attachments/Ink/Drawing/2026.5.19 - 15.54pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```

Viewing the image above, we aim to get the volume of the sphere 
We do a couple things. We first aim to get the cross section of the sphere in the Y plane (straight up)

Take an arbitrary point in the middle of the shape. To find the cross section, we need to find the radius between the x axis and f(x). We need to get R (cross sectional area) as a function of x(something we know) and the spheres radius R, something  we also know. 

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "attachments/Ink/Drawing/2026.5.19 - 15.56pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```


via Pythagorean [[theorem]] $R^2 = r^2-x^2$
Thus, we have cross sectional area defined as $A(x)=\pi y^2 = \pi(r^2-x^2)$

Thus, we obtain the volume through integration as $V = \int_{a}^bA(x)dx$


# Cylindrical shells

Sometimes, its more convenient to find the volume of a shape via a different method. \



Let $D$ be a 2d region in the plane bounded on the left by $x = a$(with $a > 0$),
on the right by $x = b$, above by $y = f (x)$ and below by $y = g(x)$. Let $E$ be the
3d region obtained by rotating $D$ through a full rotation about the y-axis. 
![[Pasted image 20260526111057.png]]
The cross section of $D$ looks like how it looks above, but note we cannot simply multiply this by a circumference to get the area. This is because every point sits at a different distance to the circumference. 

Instead we employ a method where we take a subinterval of D and rotate it around the y axis. We can do this with rectangles.

![[Pasted image 20260526111804.png]]
Rotating one of these rectangles around the y axis gives us a ring shape that simplifies almost to a rectangular prism 
![[Pasted image 20260526111842.png]]


Doing this many times gives us a shape like this (different example but the idea holds )
![[Pasted image 20260526111952.png]]

We approximate the area of a single shell as 
$2\pi ix_{i}^*[f(x_{i}*)-g(x_{i}^*)]\cdot \Delta x$
which can be visualised below 
![[Pasted image 20260526112757.png]]



This can be converted into a [[Riemann sum]], and we can turn this into a sum of these areas 

Then Volume of $E = \int_{a}^b 2\pi x[f(x)-g(x)]dx$


