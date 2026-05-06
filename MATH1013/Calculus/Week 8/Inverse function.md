Inverse [[function]]
A [[function]] has an inverse if and only if it is a [[Bijective|bijection]].

## MATH1013
## Injectivity
In this course, we treat functions as able to have inverses if they are [[Injective Function|injective]].
We test for function injectivity by algebraically manipulating the definition of injection 
Let F be a function $F:A \to B$
$\forall x_{1},x_{2} \in A\ \  x_{1}\not=x_{2} \implies f(x_{1})\not=f(x_{2})$
We can also prove via contrapositive .
Examples:
is $f(x)=\sqrt{ x }$ injective?
let$\sqrt{  x_{1}} =\sqrt{ x_{2} }$
squaring both sides, we are left with $x_{1}=x_{2}$
thus f is injective 

### Finding the inverse function

To find the inverse function, we will solve the function for x and treat $f^-1$ in respect to y. Perhaps it is easier to use the example to understand. 

$f(x)= \frac{4x-1}{2x+3}$
$\implies y = \frac{4x-1}{2x+3}$
$\implies y(2x+3)=4x-1$
$\implies 2xy+3y=4x-1$
$\implies 2xy-4x=-3y-1$
$\implies x(2y-4)=-3y-1$
$\implies x= \frac{-3y-1}{2y-4}$
Now, we have $f^{-1}(x)=\frac{-3x-1}{2y-4}$

## Graphing inverse functions
An interesting feature of inverse functions is that they appear as a reflection to the original function across the identity function. This makes it easier to graph certain inverse functions. 


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "attachments/Ink/Drawing/2026.4.29 - 10.07am.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
## [[surjective function|surjective]] functions
The requirement of surjective functions to create an inverse is also important.  We can make a function [[Bijective]] via restricting both the **domain** of the function, and as a result, the **codomain** of the function to ensure the range is the same as the codomain. 


# Properties of [[Inverse function]]s
As is standard, the [[composition of Functions|composition]] of a function and its inverse results in the identity function. 
That is, $f^{-1}(f(x))= f(f^{-1}(x))=x$

Perhaps the most important property is that if $y = f(x), \text{then} f^{-1}(y)=x)$


Another important set of properties is that [[continuous function|continuous]]ness and differentiability are conserved across inverse functions. If a function is continuous and/or differentiable, its inverse will be as well.

### [[Derivative]] of inverse function
$f^{-1}(f(x))=x$
$\iff \frac{d}{dx} f^{-1}(f(x))=\frac{d}{dx}x$
$\iff (f^{-1})' (f(x)) \times f'(x)=1$
$\iff (f^{-1})'f(x)=\frac{1}{f(x)'}$
$\iff (f^{-1})'(y)=\frac{1}{f'(f^{-1}(y))}$
Thus the final [[theorem]]
$f^{-1}(a)=\frac{1}{f'(f^{-1}(a))}$
This theorem tell us that inverse function is differentiable at a, and tells you the value. 

