Simpson's rule
This method of numerical integration instead relies on fitting parabolas to a curve. 
## Derivation 
We fit a parabola to three evenly spaced points $(x_{1},y_{1}),(x_{2},y_{2}),(x_{3},y_{3})$. The distance between these is h

Recall that a parabola has the form $ax^2+bx+c$
$\int_{-h}^h ax^2+bx+c\ dx$ = $\left[ \frac{ax^3}{3}+\frac{bx^2}{2}+cx \right]_{-h}^h$
= $\frac{h}{3}(2ah^2+6c)$
Assuming we position the parabola such that its center point is zero, the left x is -h and the right is +h
$y_{0}=ah^2-bh+c$
$y_{1}=c$
$y_{2}=ah^2+bh+c$
$\implies 2ah = y_{0}-2y_{1}+y_{2}$
Substituting into A 
$A = \frac{h}{3}(y_{0}+4y_{1}+y_{2})$

## Approximation 
$S_{n}=\frac{\Delta x}{3}[f(x_{0})+4f(x_{1})+2f(x_{2})\dots 2f (x_{n−2}) + 4f (x_{}{n−1}) + f (x_{n})]$
where $\Delta x =\frac{b-a}{n}$ and $x_i=a+i\Delta x$
**IMPORTANT**: For [[Simpson's rule]], we specifically require an even number of [[partition]]s

## Binding error 
$\exists K \in \mathbb{R} \forall x \in [a,b] |f''''(x)| \le K \implies |E_{s}|\le$$\frac{K(b-a)^5}{180n^4}$

Remember that the minimum n must be even, and a whole number. 
