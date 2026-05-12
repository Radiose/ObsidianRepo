## General exponential [[function]] 
If $a > 0$ and $x \in \mathbb{R}$, then $a^x=e^{x\ln(a)}$
A general exponential is one of the form $f(x)=a^x$.
![[Pasted image 20260512175346.png]]

Here is a good graph of general exponential functions 

Most of the properties for general exponential functions hold from [[Eulers number and the exponential|eulers number]] and the [[Natural logarithm]], with the exception of the derivative of an exponential 
$\frac{d}{dx} a^x=a^x \ln(a)$


The general rule of expressing $f(x)^{g(x)}$ is that you can either express this as $e^{g(x\ln(f(x)))}$ or $g(x)\ln(f(x))$

A quick heads up is to always restrict the domain values of any x that is in ln(x). For example, $(cos(x))^x =e^{x\ln(\cos(x))}$ is only valid as long as cos(x) is positive, which are the values from $-\frac{\pi}{2}, \frac{pi}{2}$ radians

## [[Definite integral|integration]] 
The [[Indefinite integral|antiderivative]] of $\int a^x =- \frac{a^x}{\ln(a)}+c$ as long as $a \not=1$, this is because $\frac{d}{dx}(a^x)=a^x\ln(a)$

From the general exponential, we can also define the general logarithm 
![[General logarithm]]