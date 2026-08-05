
  Let $a \in \mathbb{N}$ and $f : [a,\infty) \to [0,\infty)$ be a continuous and non-increasing function. Let $x_j = f(j), \forall j \in \mathbb{N} \cap [a,\infty)$.
Then

$$\sum_{j=a}^{\infty} x_j \text{ converges} \iff \left(\int_a^n f(x)\,dx\right)_{n \in \mathbb{N} \cap [a,\infty)} \text{ converges.}$$

# Proof
$(\Rightarrow)$ We have that $\forall n \in \mathbb{N} \cap [a,\infty)$,

$$\int_a^n f(x)\,dx = \sum_{j=a}^{n-1} \int_j^{j+1} f(x)\,dx.$$

Let $y_j = \int_j^{j+1} f(x)\,dx, \, \forall j \in \mathbb{N} \cap [a,\infty)$.
Then $\forall j \in \mathbb{N} \cap [a,\infty)$, $0 \leq y_j \leq \int_j^{j+1} f(j)\,dx = x_j$ (non increasing). Therefore $\sum_{j=a}^{\infty} y_j$ converges via [[Convergence of series#Theorem 2 (converging series bounds smaller one)|this theorem]], and so

$$\lim_{n\to+\infty} \int_a^n f(x)\,dx = \sum_{j=a}^{\infty} y_j.$$



$(\Leftarrow)$ We have that $\forall n \in \mathbb{N} \cap [a,\infty)$,

$$\int_a^n f(x)\,dx = \sum_{j=a+1}^{n} \int_{j-1}^{j} f(x)\,dx.$$

Let $z_j = \int_{j-1}^{j} f(x)\,dx, \, \forall j \in \mathbb{N} \cap [a+1,\infty)$. Then $\forall j \in \mathbb{N} \cap [a+1,\infty)$,

$$0 \leq x_j = \int_{j-1}^{j} f(j)\,dx \leq \int_{j-1}^{j} f(x)\,dx = z_j,$$(*f is non increasing*)

and so

$$\left(\int_a^n f(x)\,dx\right)_{n\in\mathbb{N}} \text{ converges} \iff \sum_{j=a+1}^{\infty} z_j \text{ converges}$$

which implies $\sum_{j=a}^{\infty} x_j$ converges. $\blacksquare$

