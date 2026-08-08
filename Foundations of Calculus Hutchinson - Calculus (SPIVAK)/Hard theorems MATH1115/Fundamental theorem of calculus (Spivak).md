---
tags:
  - spivak
---

Based off [[Integrable (spivak)#Theorem 8 |this theorem]], if $f$ is integrable, then $F(x) = \int_{a} ^x f$ is [[continuous function|continuous]]. 
We should ask then, what happens when $f$ is continuous, and it turns out $F$ is indeed differentiable. 

## The first fundamental theorem of calculus 


Let $f$ be integrable on $[a,b]$, and define $F$ on $[a,b]$ by

$$F(x) = \int_a^x f.$$

If $f$ is continuous at $c$ in $[a,b]$, then $F$ is differentiable at $c$, and

$$F'(c) = f(c).$$

(If $c = a$ or $b$, then $F'(c)$ is understood to mean the right- or left-hand derivative of $F$.)

### Proof 

We will assume that $c$ is in $(a,b)$; the easy modifications for $c=a$ or $b$ may be supplied by the reader. By definition,

$$F'(c) = \lim_{h\to 0} \frac{F(c+h) - F(c)}{h}.$$

Suppose first that $h > 0$. Then

$$F(c+h) - F(c) = \int_c^{c+h} f.$$

Define $m_h$ and $M_h$ as follows (Figure 1):

$$m_h = \inf\{f(x) : c \le x \le c+h\},$$
$$M_h = \sup\{f(x) : c \le x \le c+h\}.$$

It follows from [[Integrable (spivak)#THEOREM 7|Theorem 7]]  that

$$m_h \cdot h \le \int_c^{c+h} f \le M_h \cdot h.$$

Therefore,

$$m_h \le \frac{F(c+h)-F(c)}{h} \le M_h.$$

If $h < 0$, only a few details of the argument have to be changed. Let

$$m_h = \inf\{f(x) : c+h \le x \le c\},$$
$$M_h = \sup\{f(x) : c+h \le x \le c\}.$$


Then

$$m_h \cdot (-h) \le \int_{c+h}^c f \le M_h \cdot (-h).$$

Since

$$F(c+h) - F(c) = \int_c^{c+h} f = -\int_{c+h}^c f,$$

this yields

$$m_h \cdot h \ge F(c+h) - F(c) \ge M_h \cdot h.$$

Since $h<0$, dividing by $h$ reverses the inequality again, yielding the same result as before:

$$m_h \le \frac{F(c+h)-F(c)}{h} \le M_h.$$

This inequality is true for any integrable function, continuous or not. Since $f$ is continuous at $c$, however,

$$\lim_{h\to 0} m_h = \lim_{h\to 0} M_h = f(c),$$
(this is because $M_{h},m_{h}$ are defined in terms of $h$) 
and this proves that

$$F'(c) = \lim_{h\to 0} \frac{F(c+h)-F(c)}{h} = f(c). \qquad \blacksquare$$


This theorem provides a corollary that reduces computations to some triviality
## Corollary
If $f$ is continuous on $[a,b]$ and $f = g'$ for some function $g$, then

$$\int_a^b f = g(b) - g(a).$$

**PROOF**  Let

$$F(x) = \int_a^x f.$$

Then $F' = f = g'$ on $[a,b]$. Consequently, there is a number $c$ such that 

$$F = g + c.$$
This is some consequence of the [[mean value theorem]], if two functions have equal derivatives on an interval, they differ by some constant. 


The number $c$ can be evaluated easily: note that

$$0 = F(a) = g(a) + c,$$ because $F(a)$ has an integral $\int_{a}^af$ 


so $c = -g(a)$; thus

$$F(x) = g(x) - g(a).$$

This is true, in particular, for $x = b$. Thus

$$\int_a^b f = F(b) = g(b) - g(a). \qquad \blacksquare$$


It should be noted that this corollary is widely thought of to be the definition of an integral(that $\int_{a}^b f=g(b)-g(a)$, where the derivative to $g$ is $f$), but that's not true. For example, $\int \frac{1}{x}dx$ has no simple antiderivative. Theorem 1 states that the antiderivative of $\frac{1}{x}$ is $g(x) = \int_{1}^x \frac{1}{t}dt$, and we know no such simpler function with this property. Thus, the antiderivative is literally defined in terms of itself in a way. (in fact we know from previous study that its the [[Natural logarithm]])

This corollary is often referred to as the *second fundamental theorem of calculus*, but Spivak refers to a different, similar but slightly more useful theorem as that. 



 
## The second fundamental theorem of calculus

If $f$ is integrable on $[a,b]$ and $f = g'$ for some function $g$, then

$$\int_a^b f = g(b) - g(a).$$

**PROOF** Let $P = {t_0, \dots, t_n}$ be any partition of $[a,b]$. By the Mean Value Theorem there is a point $x_i$ in $[t_{i-1}, t_i]$ such that

$$g(t_i) - g(t_{i-1}) = g'(x_i)(t_i - t_{i-1})$$ $$= f(x_i)(t_i - t_{i-1}).$$

If

$$m_i = \inf \{f(x) : t_{i-1} \le x \le t_i\},$$ $$M_i = \sup \{f(x) : t_{i-1} \le x \le t_i \},$$

then clearly

$$m_i(t_i - t_{i-1}) \le f(x_i)(t_i - t_{i-1}) \le M_i(t_i - t_{i-1}),$$

that is,

$$m_i(t_i - t_{i-1}) \le g(t_i) - g(t_{i-1}) \le M_i(t_i - t_{i-1}).$$

Adding these equations for $i = 1, \dots, n$ we obtain

$$\sum_{i=1}^n m_i(t_i - t_{i-1}) \le g(b) - g(a) \le \sum_{i=1}^n M_i(t_i - t_{i-1}),$$

so that

$$L(f,P) \le g(b) - g(a) \le U(f,P)$$

for every partition $P$. But this means that

$$g(b) - g(a) = \int_a^b f. \qquad \blacksquare$$

The trick here was to use the mean value equality to create some $x_{i}$ that will sit between the inf and sup (bounds of the y axis) of each partition. We then can replace it with the other side of the equality and create lower and upper sums that will become an integral.

