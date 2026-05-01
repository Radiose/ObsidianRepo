---
{}
---
Integration by parts

This is the equivalent of [[Integration by substitution|U-substitution]] for the [[Product rule]]. 
#### full logic
$\frac{d}{dx}(u(x)v(x))=u'(x)v(x)+u(x)v'(x)$
$\implies u(x)v(x)+c = \int u'(x)v(x)+u(x)v'(x)\ dx$
$\implies u(x)v(x)+c = \int u'(x)v(x)\ dx = \int u(x)v'(x)\ dx$
$\implies \int u(x)v'(x)\ dx = u(x)v(x) - \int u'(x)v(x)\ dx$

Therefore the rule 
$\int u(x)v'(x) = u(x)v(x) - \int u'(x)v(x)\ dx + c$ is known as integration by parts 
When an integrand is a product of two functions, the product becomes simpler when we find the [[Indefinite integral|antiderivative]] of one and the [[Derivative]] of the other. 


