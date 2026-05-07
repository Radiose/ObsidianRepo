Natural logarithm
We define the natural logarithm as:
 $\ln(x)=\int_{1}^x \frac{1}{t}dt$
 VIA [[The fundamental theorem of calculus|FTC]] I, it is differentiable and $\frac{d}{dx} \ln(x)=\frac{1}{x}$. Thus, the natural logarithm can be thought of as the area under the curve of $\frac{1}{x}$ from 1 to the value in the natural log.
Logarithmic laws 
$\ln(x)<0$ when $x \in(0,1)$, $\ln(1)=0$,$\ln(x)>0$ when $x \in(1,\infty)$
$\ln(ab)= \ln(a)+\ln(b)$
$\ln{\frac{1}{b}}= -\ln(b)$
$\ln\left( \frac{a}{b} \right)=\ln a-\ln b$
$\ln a^r=r\ln(a)$


# Use in [[Derivative]]s and [[Definite integral|integration]]

A [[composition of Functions|composition]] between ln and another function $\ln(g(x))$ is generally assumed to be defined/restricted on some interval that the result of g(x) lies in the domain of ln(x)
Because the derivative of ln(x) = $\frac{1}{x}$, we can use the chain rule to derive $\ln(f(x))=\frac{f'(x)}{f(x)}$

## Integration
Because of this, integrands with the form $\int \frac{f'(x)}{f(x)}dx$ = $\ln|f(x)| + c$
NOTE: REMEMBER TO TAKE THE ABSOLUTE VALUE 

A useful example $\int \tan x \ dx= \int \frac{\sin}{\cos} = \int- \frac{f'x()}{f(x)}dx$ = $-\ln|\cos(x)|+c$

# Differentiation
Typically when using the [[Chain rule]], its easy when functions are raised to constant powers, but if the equation has the form $y = (f(x))^{g(x)}$ , its a bit more complicated. 
Thus, we can use [[Natural logarithm]]s

$y = x^{\sin x}$
$\ln(y)=\ln(x^{\sin (x)})$ Note that we restrict $x^{sin(x)}$ to be greater than 0 via $\sin(x)\ \ x\in(0,\pi)$ so that x is in the domain of ln
$\iff \ln(y)= \sin(x)\ln(x)$
$\iff \frac{1}{y} \frac{dy}{dx}=\frac{d}{dx}{\sin(x)\ln(x)}$
$\iff \frac{dy}{dx}=\left( \cos(x)\ln(x)+\frac{\sin(x)}{x} \right) \times y$
$\iff \frac{dy}{dx}=\left( \cos(x)\ln(x)+\frac{\sin(x)}{x} \right) \times x^{\sin(x)}$
