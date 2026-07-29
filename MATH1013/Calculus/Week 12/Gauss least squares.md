Gauss least squares

This is a method of [[Interpolation]] to fit a [[set]] of data points to an equation 


# Iodine decay 
After 36 hours, we have the following graph. Initial $C_{0}=100$

![[Pasted image 20260526153815.png]]

There are 36 data points on this, and it looks like an exponential can possibly fit it


![[Pasted image 20260526153742.png]]


So, we have $ln(yi)=\ln C_{0}+kt_{i}$

The gauss least squares method finds the best t and b for the formula  $f(t) = kt+b$

We have the formula Error(k, b) = $\frac{1}{37}$$\sum_{i=0}^{36}(kt_{i}+b-\ln(y_{i}))^2$

The $\hat{k}\hat{b}$ that minimise the error are the least squares estimator and the line that best fits the line is $\hat{f}(t)=\hat{k}t+\hat{b}$

continuing 
$$ \begin{aligned} 37\,\text{Error}(k,b) &= \sum_{i=0}^{36} \left((kt_i + b) - \ln y_i\right)^2 \\[4pt] &= \sum_{i=0}^{36} (kt_i + b)^2 - 2(kt_i + b)\ln y_i + (\ln y_i)^2 \\[4pt] &= \sum_{i=0}^{36} k^2 t_i^2 + 2kbt_i + b^2 - 2kt_i \ln y_i - 2b \ln y_i + (\ln y_i)^2 \\[4pt] &= k^2 \sum_{i=0}^{36} t_i^2 + 37b^2 + 2kb \sum_{i=0}^{36} t_i - 2k \sum_{i=0}^{36} t_i \ln y_i - 2b \sum_{i=0}^{36} \ln y_i + \sum_{i=0}^{36} (\ln y_i)^2 \\[4pt] &:= S(t^2)\,k^2 + 37b^2 + 2S(t)\,kb - 2S(t\ln y)\,k - 2S(\ln y)\,b + S((\ln y)^2) \end{aligned} $$
We then get the [[derivative]] of this in terms of $b$ to find the global minimum and do [[The first Derivative test]]

$$ \begin{aligned} h'(b) &= \frac{1}{37}\frac{d}{db}\left(S(t^2)\,k^2 + 37b^2 + 2S(t)\,kb - 2S(t\ln y)\,k - 2S(\ln y)\,b + S(\ln y^2)\right) \\[4pt] &= 2b + \frac{2}{37}S(t)\,k - \frac{2}{37}S(\ln y) \end{aligned} $$
Now we find when h'(b)=0
$$ \begin{aligned} h'(b) = 0 &\iff 2b + \frac{2}{37}S(t)\,k - \frac{2}{37}S(\ln y) = 0 \\[4pt] &\iff \hat{b} = \frac{S(\ln y) - S(t)\,k}{37} \end{aligned} $$
We also do the same thing for k

In summary, we have that the best slope and intercept should satisfy:

$$
\hat{k} = \frac{S(t\ln y) - S(t)\,b}{S(t^2)} \qquad\qquad \hat{b} = \frac{S(\ln y) - S(t)\,k}{37}
$$

Substituting $\hat{b}$ into the expression for $\hat{k}$ we obtain

$$
\hat{k} = \frac{S(t\ln y) - S(t)\cdot\dfrac{S(\ln y) - S(t)\,\hat{k}}{37}}{S(t^2)}
$$

which by some algebra implies that

$$
\hat{k} = \frac{S(t\ln y) - \tfrac{1}{37}S(t)\,S(\ln y)}{S(t^2)}\left(1 + \frac{S(t)}{37\,S(t^2)}\right)^{-1}
$$

and substituting the value of $\hat{k}$ in $\hat{b}$ we obtain the value of $\hat{b}$.

Putting these into the original formula 
We get rid of the ln for y. We also 

$C(t) = 93.2421 × e^{−0.1025×t}$, as e^b is a constant, 
