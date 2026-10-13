# Vector valued functions 

Let $a,b \in \mathbb{R} : b>a$
let $x \in[a,b]\to \mathbb{R}^n$ be continuous 
Let $f:\mathbb{R}^n\to \mathbb{R}$ and $F:\mathbb{R}^n\to \mathbb{R}^n$ be [[multivariate continuity|continuous]].
Define $\mathcal{C}:=\{ x(t)  \in \mathbb{R}^n ; t \in[a,b] \}$, a [[vector valued curve]]

We define 
$$\int_{a}^b x(t)dt:=\left( \int_{a}^b x(t)\cdot e_{1}dt ,\dots,\int_{a}^b x(t)\cdot e_{n} \right)$$
$$\int_{\mathcal{C}} F(x) \cdot dx :=\int F(x(t))\cdot x'(t)dt \in \mathbb{R}$$
$$\int_{\mathcal{C}}f(x)dx:= \int_{a}^b f(x(t))x'(t)dt \in \mathbb{R}^n$$
Intuitively, this can be established from $\frac{dx}{dt}=x'(t),$ so $dx=x'(t)dt$ (not mathematically, but intuitively), where the variation on the curve, can be bought back to the variation of the parameter $t$, that you multiply by $x'(t)$. Or even simpler, the $dx$ gets changed into $x'(t)dt$.

## Remark
Look at the third integral we have. The same concept of [[The fundamental theorem of calculus]] applies to this one, where we are summing up the changes in the tangent [[vector]] $x'(t)dt$.





![[arc length parametrisation]]

# One dim codomain 

Let $\prod_{j=1}^n \left[ a_{j},b_{j} \right]=R$ 
We define $$1_{\prod_{j=1}^n [a_{j},b_{j}]} :\mathbb{R}^n \to \mathbb{R} \\x \mapsto \begin{cases}
1,\quad x \in {R} \\
0,\ \ \ \ \text{otherwise}
\end{cases}$$
Additionally, $\int_{\mathbb{R}^n}1_{\prod_{j=1}^n [a_{j},b_{j}]}(x)dx:= \prod_{j=1}^n \lvert b_{j}-a_{j} \rvert=:\int_{\prod_{j=1}^n [a_{j},b_{j}]}dx=: \int _{a_{n}}^{b_{n}}\dots\int_{a_{1}}^{b_{1}}dx_{1}\dots dx_{n}$

