this applies to convex [[function]]s. A function is convex if when you take points between an interval, they are lower in $y$ values than the line you draw over it.

 ![InkDrawing](<attachments/Ink/Drawing/2026.8.24 - 17.23pm.svg>) [Edit Drawing](https://youtu.be/2arL1jh8ihA?type=inkDrawing&width=500&aspectRatio=1.778&viewBoxX=0&viewBoxY=0&viewBoxW=2000&viewBoxH=1125)
this function is concave on its entire domain.

With that said
# Definition 
If $f$ is a convex function and $X$ is a [[random variable]], then $f(\mathbb{E}[X])\leq \mathbb{E}[f(X)]$
Moreover, $f$ is strictly convex, $X=\mathbb{E}[X]$

In other words, for a probability [[vector]] $\mathbf{p}$
$f \left(\sum_{i=1}^N p_{i}x_{i} \right) \leq \sum_{i-1}^N p_{i}f(x_{i})$	

and for a concave function $f(\mathbb{E}[X])\geq \mathbb{E}[f(X)]$
