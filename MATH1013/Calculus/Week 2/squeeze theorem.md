---
{}
---
The squeeze [[theorem]] 

[[limits|limit]] of a [[Sequence]] definition:
Let $a_{n},b_{n},c_{n}$ be sequences. 
suppose $a_{n} \le b_{n} \le c_{n}$ ultimately. Suppose $a_{n} \to L$ and $c_{n} \to L$. Then $b_{n}\to L$

## Proof

Suppose $a_n \leq b_n \leq c_n$ ultimately. Suppose $a_n \to L$ and $c_n \to L$. Let $\varepsilon > 0$ be given. Since $a_n \to L$ there is some integer $N_1$ such that $$n > N_1 \Rightarrow a_n \in (L - \varepsilon, L + \varepsilon). \tag{21}$$ Since $c_n \to L$ there is some integer $N_2$ such that $$n > N_2 \Rightarrow c_n \in (L - \varepsilon, L + \varepsilon). \tag{22}$$ Let $N = \max\{N_1, N_2\}$. Then since $a_n \leq b_n \leq c_n$ it follows from $(21)$ and $(22)$ that $$n > N \Rightarrow b_n \in (L - \varepsilon, L + \varepsilon).$$ But $\varepsilon$ was an arbitrary positive number, and so it follows that $b_n \to L$. $\blacksquare$




Applied context to [[function]]s:

let f(x), g(x), h(x) be functions
IF
1:f(x)$\le$g(x)$\le$h(x) when $x \in N(a, \delta)$
2: $\lim_{ x \to a }f(x)=\lim_{ x \to a }h(x)=L$
Then $\lim_{ x \to a }g(x)=L$

You can conclude that the middle function is equal to the left and the right limits if and only if all values of of x have 

