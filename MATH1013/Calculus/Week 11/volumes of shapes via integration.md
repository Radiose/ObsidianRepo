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

Sometimes, 

Let $D$ be a 2d region in the plane bounded on the left by $x = a$(with $a > 0$),
on the right by $x = b$, above by $y = f (x)$ and below by $y = g(x)$. Let $E$ be the
3d region obtained by rotating $D$ through a full rotation about the y-axis.
Then Volume of $E = \int_{a}^b 2\pi x[f(x)-g(x)]dx$



