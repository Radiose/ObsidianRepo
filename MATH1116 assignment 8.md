1:
Recall that $$\int_{\mathcal{C}}f(x)dx:=\int_{a}^b f(x(t))x'(t)dt$$ for $x(t)\in \mathcal{C},f(x):[a,b]^d \to\mathbb{R}$

Thus, $$\int_{\{ x_{n}(t)|t \in{0,1} \}}f(x)dx=\int_{0}^1 f(x_{n}(t))x_{n}'(t)dt$$
If we prove that $f(x_{n}(t))x_{n}'(t)$ is uniformly convergent, then we can take the limit of the inside of the integral and get the convergence simply. 

Define $x(t):=\lim_{ n \to \infty }x_{n}(t)$

Let $\epsilon=1$, then $\exists N\ \ n > N \implies\lVert x_{n}(t)-x(t) \rVert<1$

Define A $:= max(\lVert x_{1}(t) -x(t)\rVert_{\infty},\dots,\lVert x_{N}(t)-x(t) \rVert_{\infty})$


Define $G:= max(1,A)$
Define $C$ as the upper bound on $f$, from its continuity.

Additionally, note that because $f$ is uniformly continuous (it has a closed interval as domain and is continuous on it), 
$\forall\epsilon >0\  \exists\delta > 0\ \forall t,t_{0}\in[0,1]^d\ \ \lvert t-t_{0} \rvert<\delta \implies |f(t)-f(t_{0})|<\epsilon$.


For this reason we can choose $N$ such that $m,n>N$ has $||x_{n}(t)-x_{m}(t)||_{\infty}<\delta \quad \forall t$ by uniformly Cauchy. Then, $\forall \epsilon > 0$, $\exists N\quad\forall n,m>N$$\lVert f(x_{n}(t))-f(x_{m}(t)) \rVert_{\infty}<\epsilon$.

So, 

let $\epsilon_{2} >0$. Choose $N$ such that 

$\forall n,m>N,\quad \lVert f(x_{n}(t))-f(x_{m}(t)) \rVert_{\infty}< \frac{\epsilon_{2}}{2G}$
and $\lVert x'_{n}(t)-x'_{m}(t) \rVert_{\infty}< \frac{\epsilon_{2}}{2C}$

Then, $\lVert f(x_{n}(t))\cdot x'_{n}(t) -f(x_{m}(t))x'_{m}(t)\rVert_{\infty} = \lVert x'_{n}(f(x_{n}(t))-f(x_{m}(t)))+f(x_{m}(t))(x'_{n}(t)-x'_{m}(t)) \rVert_{\infty}$

$\leq \lVert G(f(x_{m}(t))-f(x_{n}(t))) \rVert_{\infty} + \lVert C(x'_{n}(t)-x'_{m}(t)) \rVert_{\infty} < \frac{\epsilon_{2}}{2}+\frac{\epsilon_{2}}{2}$ thus uniformly cauchy.

Because of this, $\lim_{ n \to \infty }\int_{0}^1 f(x_{n}(t))x_{n}'(t)dt=\int_{0}^1\lim_{ n \to \infty }f(x_{n}(t))x'_{n}(t)dt=\int_{0}^1 f(x(t))x'(t)$, where $x(t)$ and $x'(t)$ are the limits of $x_{n}(t)$ and $x'_{n}(t)$.
Thus, the sequence is convergent.




2:
we define $$g(t) \begin{cases}
f(t), & \text{if t }\in \mathbb{R^*}
\\ (0,1/2), & \text{otherwise}
\end{cases}$$
as the extension of $f(t)$.

We check that is it continuous. If $\lim_{ t \to 0 }f(t)=\left( 0,\frac{1}{2} \right)$, then we know that the function is continuous. 
Via the lecture notes, if $\lim_{ x \to \infty }\frac{x-\sin(x)}{x^2}=0$, $\lim_{ x \to 0 } \frac{1-\cos x}{x^2}=0$, then $g(t)$ is continuous. 

$\lim_{ x \to 0 } \frac{x-\sin(x)}{x^2}=\lim_{ x \to 0 } \frac{1-\cos(x)}{2x}=\lim_{ x \to 0 }\frac{\sin(x)}{2}=0$ via differentiability of numerator and denominator, and L'Hopital's rule. 

Similarly, $\lim_{ x \to 0 }\frac{1-\cos(x)}{x^2}= \lim_{ x \to 0 }\frac{\sin(x)}{2x}=\lim_{  x \to 0 }\frac{\cos(x)}{2}=\frac{1}{2}$ because each of the numerators and denominators were differentiable, thus we used L'Hopital's. 


Now we show it has an axis of symmetry about the $y$ axis. Call $x(t) := \frac{t-\sin(t)}{t^2}$, $y(t):=\frac{1-\cos(t)}{t^2}$

$\forall t\in \mathbb{R},\exists t_{2}\in \mathbb{R}\quad x(t)=-x(t_{2}),\ \ y(t)=y(t_{2})$ 
Let $t \in \mathbb{R}$
Choose $t_{2}=-t$
Note that $sin(t)$ is "odd", so by definition, so $\sin(-t)=-\sin(t)$

$\implies t-\sin(t)=t+\sin(-t)$
$\implies t-\sin(t)=-1 \left( (-t)- \sin(-t)\right)$
$\implies \frac{t-\sin(t)}{t^2}=-1\left( \frac{(-t)-\sin(-t)}{t^2} \right)$

$\implies x(t)=-(x(-t))$ (because $(-t)^2=t^2$)

And additionally, $\cos(t)=\cos(-t)$ by definition. 
$\implies 1-\cos(t)=1-\cos(-t)$
$\implies\frac{{1}-\cos(t)}{t^2}=\frac{1-\cos(-t)}{t^2}$ 
So, $g(t)$ has an axis of symmetry about the $y$ axis. 




3:
A: we aim to find A and B that don't commute. We can take $A=\begin{bmatrix}1 & 0 \\  1 & 1\end{bmatrix}$, $B=\begin{bmatrix}3  &  5  \\  4 & 6\end{bmatrix}$. We show they don't commute with an example $AB \begin{bmatrix}1 \\ 0 \end{bmatrix}=\begin{bmatrix} 7 \\  4\end{bmatrix}$, $BA \begin{bmatrix}1  \\  0\end{bmatrix}=\begin{bmatrix}1  \\  1\end{bmatrix}$

B:
Because $(e^A)^{-1}\cdot e^A=I$, it will suffice to show that $e^{-A}\cdot e^{A}=I$

First we establish that $A$ and $-A$ commute via the properties of matrix associativity:

$A(-{A})\mathbf{v}=A(-{A}\mathbf{v})$ via properties of linear maps
$=A((-1)A\mathbf{v})=(-(1){A})(A\mathbf{v})=-A(A(\mathbf{v}))=-AA(\mathbf{v})$

This implies that $e^{-A}e^{A}=e^{-A+A}=e^{0}=I+\sum_{n=1}^\infty \frac{0^n}{n!}=I$

C:
$e^A=e^{\lambda I+N}$
We show $\lambda I,N$
Therefore $e^A=e^{\lambda I}\cdot e^N$
If $N$ is k dimensional, we have $e^{N}$ is a matrix with $1$ on the diagonal and super diagonal, $\frac{1}{2}$ on the diagonal above that repeating until $\frac{1}{k!}$ is in the top right corner.

 ![InkDrawing](<attachments/Ink/Drawing/2026.10.6 - 14.38pm.svg>) [Edit Drawing](https://youtu.be/2arL1jh8ihA?type=inkDrawing&width=500&aspectRatio=1.778&viewBoxX=0&viewBoxY=0&viewBoxW=2000&viewBoxH=1125)

Then, multiplying it by $e^{\lambda I}=\sum \frac{(\lambda I)^n}{n!}=I \cdot \sum\frac{\lambda^n}{n!}=I\cdot e^\lambda$ where $e^\lambda \in \mathbb{R}$.
Thus, $e^A$ looks like 
 ![InkDrawing](<attachments/Ink/Drawing/2026.10.6 - 14.43pm.svg>) [Edit Drawing](https://youtu.be/2arL1jh8ihA?type=inkDrawing&width=500&aspectRatio=1.778&viewBoxX=0&viewBoxY=0&viewBoxW=2000&viewBoxH=1125)
d:

This can be done because by representing $A=EJE^{-1}$, getting $e^A=e^{EJE^{-1}}$
$=I+ \sum \frac{(EJE)^{n}}{n!}$
Note that $(EJE^{-1})^n=(EJE^{-1})(EJE^{-1})\dots=EJIJI\dots JIE^{-1}$
$\implies I+ \sum \frac{(EJE)^n}{n!}$ $=I+\sum\frac{EJ^nE^{-1}}{n!}$
$=E e^JE^{-1}$
Thus, getting $e^A$ is just about getting $e^J$ and from there multiplying it accordingly to the equation above. 


4:
a: The trace of this matrix is defined as $\sum d_{i}\lambda_{i}=4+3+4=11$
The determinant is $\prod \lambda_{i}^{d_{i}}=4 * 3 * 4=48$
b:
The eigenvalues are 2, with algebraic multiplicity 2, 3 with AM 1, and 4 with AM 1.
c:
No. We only know if $A$ is diagonalisable if we know that it has a basis of eigenvectors. We need to know if $\dim(E(2,A))=2$. If so, its diagonalisable.

d:
We first get the basis of $\ker(A-2I)$
$=\ker\left( \begin{bmatrix}4  & -2 & 2 & -2 \\  3 & -1  & 1 & -1 \\  4 & -3 & 2 & -1 \\  5 & -4 & 3 & -2\end{bmatrix} \right)$ 
After gaussian elimination, we get $\begin{bmatrix} 1  & 0 & 0 & 0 \\  0 & 1 & 0 & -1  \\  0 & 0 & 1 & -2  \\  0 & 0 & 0 & 0 \end{bmatrix}$ and obtain basis $\{ t \begin{bmatrix}0 \\  1 \\  2 \\  1\end{bmatrix}| t \in \mathbb{R} \}$
Because the dimension of this is $1$, we know therefore that $A$ is not diagonalisable, as $E(\lambda_{1},T)+\dots+E(\lambda_{n},T)$ is not a direct sum (also it must have 3 distinct eigenvalues) .


Similarly, $A-3I$ will result in $$
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & -1 & 1 \\
0 & 0 & 0 & 0
\end{bmatrix}$$via gaussian elimination, giving basis $\{ t\begin{bmatrix}0 \\  0 \\  1 \\  1\end{bmatrix} |t\in \mathbb{R}\}$. All eigenvectors with associated eigenvalue $3$ will be of this form. 

Finally, we get the eigenspace of eigenvalue $4$. We want $$\ker(\begin{bmatrix}2	& -2&	 2	&-2\\
3&	-3&	 1&	-1\\
4&	 3&	-1&	-1\\
5	&-4&	 3&	-4\end{bmatrix})$$ So after gaussian elimination, we achieve REF of $$\begin{bmatrix}
1 & 0 & 0 & -1 \\
0 & 1 & 0 & -1 \\
0 & 0 & 1 & -1 \\
0 & 0 & 0 & 0\end{bmatrix}$$
and from here we obtain basis of its kernel as $\{ t\begin{bmatrix}1 \\  1 \\  1 \\  1\end{bmatrix} |t\in \mathbb{R}\}$ so all eigenvectors are of this form with associated E-value of $4$.

e:
We use the algorithm documented in the notes. 
Eigenvalues 3 and 4 already have $\dim(A-\lambda I)=$ their multiplicative identities, so we need to the basis of $\ker((A-\lambda I)^2)$ which gives us $\{ a\begin{bmatrix}1  \\  0 \\  0 \\  2\end{bmatrix},b \begin{bmatrix}0  \\  1  \\  2  \\  1\end{bmatrix} \}$

Thus, our total Jordan basis is $\{ \begin{bmatrix}0  \\  1  \\  2  \\  1\end{bmatrix}, \begin{bmatrix}1  \\  0 \\  0 \\  2\end{bmatrix},\begin{bmatrix}0  \\  0 \\  1 \\  1\end{bmatrix},\begin{bmatrix}1  \\  1  \\  1  \\  1\end{bmatrix}\}$ 

and our jordan normal form is $\begin{bmatrix}2  & 1 & 0 & 0 \\  0 & 2 & 0 & 0 \\0 & 0 & 3 & 0 \\  0 & 0 & 0 & 4  \end{bmatrix}$


5: Reflection statement 
I used AI to help me work my way through problems. In particular, I produced one solution for question 1 and it turned out to be wrong because I misunderstood some principles of uniform convergence. This was very helpful and after it showed me my error, I redid my proof using a method that will actually work. For question 2, I used the internet to give me the statement for axis of symmetry. I could come up with the main idea of the statement, but it is much easier when you have the actual statement in front of you to prove. 

I used AI to also help me solve part of question 3. It was a simple sum manipulation but I was going about it the wrong way and was incorrectly applying principles of analysis to linear algebra. Finally, I used AI to double check my row reductions were correct for question 4. I could have done this myself but I was feeling lazy. 

I used help from my tutor during the workshop for question 2. 

For the exams:
Question 1: I understand the principles behind this, but I am not sure I would be able to solve it in an exam under time pressure. This is a familiar theme with this weeks problems. It possibly shows a lack of complete understanding. 
2: I would be able to solve this in an exam, but I would probably not be able to make some parts of it as rigorous because I did not come up with statement myself. Again, it did say "show" instead of prove so I could probably informally show the axis did exist. 
3: I would be able to solve most of this in an exam, but probably not completely or fully rigorously. Time crunch would also be a problem.

4: I would not be able to solve a similar question in an exam currently, this is mainly because I have not memorised the JNF algorithm fully. I will need to spend time remembering how to actually get the JNF. The previous parts are also shaky(diagonalisable operators, eigenspace dimensions). I need more time working with that area of LA. 