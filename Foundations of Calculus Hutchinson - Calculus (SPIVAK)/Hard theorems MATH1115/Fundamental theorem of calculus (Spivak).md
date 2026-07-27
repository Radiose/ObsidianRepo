
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



The second fundamental theorem of calculus 