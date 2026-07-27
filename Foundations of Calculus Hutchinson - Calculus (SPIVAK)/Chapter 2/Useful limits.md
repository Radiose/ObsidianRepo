Below are some useful [[limits|limit]]s. I'm not quite sure about where they should fit in the vault yet. 

(1) if $|x| < 1$, then $\lim_{ }x^n=0$
(2) if $x$ is any [[real number]], then $\lim_{  } \frac{x^n}{n!}=0$

Proof of 1:
Since $|x| <1$ the [[Sequence]] $x_{n}$ is decreasing and all terms are $>0$
Hence, $|x|^n \to a$, and thus by [[properties of sequence limits]], $|x|^n+1 \to a$ as well.
$\implies |x|^n=a$ and $|x|^{n+1} = a$
$\iff |x|^{n+1}=|x||x|^n \to |x|a$
Hence $a = |x|a$ (uniqueness of sequence limits)
This is only possible if $a = 0$, thus, $\lim_{ n \to \infty }|x|^n=0$ ($x \not=0$) when $|x|<1$
Because $-|x|^n\leq x^n \leq |x|^n$, then via [[squeeze theorem]], $\lim_{ n \to \infty }x^n=0$
