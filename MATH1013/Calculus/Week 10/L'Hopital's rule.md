L'Hopital's rule
Certain types of indeterminant forms are usable for [[limits|limit]]s, and others aren't.
The indeterminant forms $\frac{\pm\infty}{\pm \infty}$ and $\frac{0}{0}$ are the forms that we want. $(\infty-\infty)$ or $1^\infty$ are the less desired ones. The basis of  [[L'Hopital's rule]] is changing the less desired to the more desired so that we can then simplify them via the [[derivative]].

[[theorem]]
Suppose f, g are differentiable and $g'(x) \not=0$ near $a$ except possibly at $a$
Suppose that 
$\lim_{ x \to a }f(x)=0$ and $\lim_{ x \to a }g(x)=0$
or 
$\lim_{ x \to a } f(x) = \pm \infty$ and $\lim_{ x \to a } g(x) = \pm \infty$

Then 
$\lim_{ x \to a }\frac{f(x)}{g(x)} = \lim_{ x \to a }\frac{f'(x)}{g'(x)}$


Example 
$\lim_{ x \to \left( \frac{\pi}{2} \right)^- }(\sec x-\tan(x))$
Taking the limit of this directly is $(\infty-\infty)$, which is a bad indeterminant
However using simple [[Proof of all trigonometric identities|trig identity]]s
$\lim_{ x \to \left( \frac{\pi}{2} \right)^- }\left( \frac{1}{\cos(x)}-\frac{\sin(x)}{\cos(x)} \right)$
$\implies \lim_{  x \to \left( \frac{\pi}{2} \right)^- }\left( \frac{1-\sin(x)}{\cos(x)} \right)$ - this is in the form $\frac{0}{0}$. which means we use [[L'Hopital's rule]] (taking derivative)

$\lim_{ x \to \frac{\pi}{2}^- }\frac{-\cos(x)}{-\sin x}$ = $\frac{0}{-1}=0$

