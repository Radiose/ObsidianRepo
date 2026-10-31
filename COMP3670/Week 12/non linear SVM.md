Recall [[SVM|support vector machine]]s.
Often, data is possible to be separated, but not with a hyperplane.

# Mapping to a new vector space 
The idea of nonlinear SVMs is to keep the linear classifier idea, but instead to change the representation of points. 
Say we wanted to separate data with a *circle*, rather than a line. 
![[Pasted image 20261031133647.png]]

The function will output $+1$ if $x_{1}^2+x_{2}^2 >r^2$

So, we can turn this into a linear problem if we transform $x_{1},x_{2}$ into $x_{1}^2,x_{2}^2$

# The equation 
$J(\mathbf{w},b)= \frac{1}{2}\lVert \mathbf{w} \rVert^2+ C \sum_{i=1}^N \max \{ 0,1-yi(\langle \mathbf{w}, \phi)\mathbf{x_{i}} \rangle+b) \}$
The equation is still convex, and a hyperplane is created in the new vector space. Interpreted in the old [[vector space]], this becomes a curved boundary.



# More maps
Take a single dimension example 
![[Pasted image 20261031135417.png]]
There is no linear function that can separate these data pieces correctly.
However, by using $\phi: \mathbb{R} \to \mathbb{R}^2\\ \quad \quad\quad\quad \quad\quad\quad \quad\quad (x) \mapsto(x,x^2)$, we can use a straight line to separate the features. 
![[Pasted image 20261031135621.png]]
This line is saying if $x^2<4x-3$, then assign $+1$.


![[Pasted image 20261031133647.png]]

Going back to the circle, we can also make another $\phi$, ![[Pasted image 20261031140159.png]]