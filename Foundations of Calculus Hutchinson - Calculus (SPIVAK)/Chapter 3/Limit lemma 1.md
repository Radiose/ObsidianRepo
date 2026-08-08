---
tags:
  - spivak
---
**LEMMA** for [[limits|limit]]s, involving [[absolute value]]s ($\epsilon,\delta$).


**(1)** If
$$|x - x_0| < \frac{\varepsilon}{2} \quad \text{and} \quad |y - y_0| < \frac{\varepsilon}{2},$$
then
$$|(x + y) - (x_0 + y_0)| < \varepsilon.$$

**(2)** If
$$|x - x_0| < \min\left(1, \frac{\varepsilon}{2(|y_0| + 1)}\right) \quad \text{and} \quad |y - y_0| < \frac{\varepsilon}{2(|x_0| + 1)},$$
then
$$|xy - x_0 y_0| < \varepsilon.$$

**(3)** If $y_0 \neq 0$ and
$$|y - y_0| < \min\left(\frac{|y_0|}{2}, \frac{\varepsilon |y_0|^2}{2}\right),$$
then $y \neq 0$ and
$$\left| \frac{1}{y} - \frac{1}{y_0} \right| < \varepsilon.$$
**
**PROOF**

**(1)**
$$|(x+y) - (x_0+y_0)| = |(x-x_0) + (y-y_0)| \leq |x-x_0| + |y-y_0| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon.$$

**(2)** Since $|x - x_0| < 1$ we have
$$|x| - |x_0| \leq |x - x_0| < 1,$$
so that
$$|x| < 1 + |x_0|.$$

Thus
$$
\begin{aligned}
|xy - x_0 y_0| &= |x(y - y_0) + y_0(x - x_0)| \\
&\leq |x| \cdot |y - y_0| + |y_0| \cdot |x - x_0| \\
&< (1 + |x_0|) \cdot \frac{\varepsilon}{2(|x_0| + 1)} + |y_0| \cdot \frac{\varepsilon}{2(|y_0| + 1)} \\
&< \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon.
\end{aligned}
$$

**(3)** We have
$$|y_0| - |y| \leq |y - y_0| < \frac{y_0}{2},$$
so $|y| > |y_0|/2$. In particular, $y \neq 0$, and
$$\frac{1}{|y|} < \frac{2}{|y_0|}.$$

Thus
$$\left| \frac{1}{y} - \frac{1}{y_0} \right| = \frac{|y_0 - y|}{|y| \cdot |y_0|} < \frac{2}{|y_0|} \cdot \frac{1}{|y_0|} \cdot \frac{\varepsilon |y_0|^2}{2} = \varepsilon. \blacksquare$$