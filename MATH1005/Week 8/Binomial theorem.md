Binomial [[theorem]]

The binomial [[theorem]] states that $(x+y)^n = \begin{pmatrix}n  \\  0\end{pmatrix}y^nx^n + \begin{pmatrix} n  \\ 1\end{pmatrix}y^{n-1}x^{1}+\dots+ \begin{pmatrix} n  \\  n\end{pmatrix} y^0 x^n$
So the coefficient is a product of n [[combination|choose]] some value. 

The idea 
(x+y)(x+y)(x+y)

We are basically asking how many subsets are there of this binomial with 0 xs, how many with 1 x, how many with 2 xs then finally 3 xs.
![[Pasted image 20260503164334.png]]
The image above shows the concept. We are looking for the amount of subsets with 1x out of a set of 3. 



It can be easier to visualise as [[Pascals triangle]]

![[Pascals triangle]]

# Size of the [[Sample space]] of the [[Binomial theorem]]
The size of the sample space of n events is given via $\begin{pmatrix} n \\ 0\end{pmatrix}+\begin{pmatrix}n \\ 1\end{pmatrix}+\dots+\begin{pmatrix}n  \\ n\end{pmatrix}$
This can be given simpler via $2^n$
This makes sense, as there are two outcomes for each event, and n events, gives you $2^n$

So for example the probability of obtaining exactly 3 heads from 6 tosses of a coin is given via 
$\frac{|E_{3}|}{|S|}$=$\frac{\begin{pmatrix}6  \\  3\end{pmatrix}}{2^6}$=516   


### Unfair coin example 
The general binomial [[Density function]] for *k* successes out of *n* trials with a probability P of success on each trial is given by $P(k \ \ successes)=\begin{pmatrix}n  \\ k\end{pmatrix}p^k(1-p)^{n-k}$
