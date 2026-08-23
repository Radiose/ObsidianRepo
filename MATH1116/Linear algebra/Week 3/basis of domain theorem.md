Suppose $X=\{ \mathbf{v}_{1},\mathbf{v}_{2}\dots \mathbf{v_{n}} \}$ is a basis of a vector space $V$. Suppose $\mathbf{w}_{1},\mathbf{w}_{2}\dots \mathbf{w}_{m}\in W$.
Then there exists some unique linear map $T:V \to W$ such that $T(\mathbf{v}_{j})=\mathbf{w}_{j}$ for each $j=1,\dots,n$.
### Proof 
#### Existence:
Given $\mathbf{v}\in V$, it has a basis decomposition $\mathbf{v}=a_{1}\mathbf{x}_{1}+\dots+a_{n}\mathbf{x_{n}}$ for some $a_{i}\in \mathbb{F},x_{i}\in X$
Let $T(\mathbf{v}):=a \mathbf{w}_{x_{1}}+\dots+a_{n}\mathbf{w}_{x_{n}}$.
We verify [[linearity]]
Let $\mathbf{v}=a_{1}\mathbf{x}_{1}+\dots+a_{n}\mathbf{x_{n}},\mathbf{u}=b_{1}\mathbf{x}_{1}+\dots+b_{n}\mathbf{x_{n}}$
$$
\begin{aligned}
T(\mathbf{u}+\mathbf{v}) &= T\big((a_1+b_1)\mathbf{v}_1 + \cdots + (a_n+b_n)\mathbf{v}_n\big) \\
&= (a_1+b_1)\mathbf{w}_1 + \cdots + (a_n+b_n)\mathbf{w}_n \\
&= (a_1\mathbf{w}_1 + \cdots + a_n\mathbf{w}_n) + (b_1\mathbf{w}_1 + \cdots + b_n\mathbf{w}_n) \\
&= T(\mathbf{u}) + T(\mathbf{v}).
\end{aligned}
$$

Similarly, if $\lambda \in \mathbb{F}$ and $\mathbf{v} = b_1\mathbf{v}_1 + \cdots + b_n\mathbf{v}_n$, then

$$
\begin{aligned}
T(\lambda \mathbf{v}) &= T(\lambda b_1 \mathbf{v}_1 + \cdots + \lambda b_n \mathbf{v}_n) \\
&= \lambda b_1 \mathbf{w}_1 + \cdots + \lambda b_n \mathbf{w}_n \\
&= \lambda(b_1\mathbf{w}_1 + \cdots + b_n\mathbf{w}_n) \\
&= \lambda T(\mathbf{v}).
\end{aligned}
$$
#### Uniqueness
Suppose $T \in \mathcal{L}(V,W)$ and that $T(\mathbf{v}_j) = \mathbf{w}_j$ for $j = 1,\dots,n$. Let $c_1,\dots,c_n \in \mathbb{F}$. The linearity of $T$ implies that

$$
T(c_1\mathbf{v}_1 + \cdots + c_n\mathbf{v}_n) = c_1\mathbf{w}_1 + \cdots + c_n\mathbf{w}_n.
$$

Thus $T$ is uniquely determined on $\text{span}\{\mathbf{v}_1,\dots,\mathbf{v}_n\}$. Because $\{\mathbf{v}_1,\dots,\mathbf{v}_n\}$ is a basis, we know $\text{span}\{\mathbf{v}_1,\dots,\mathbf{v}_n\} = V$. Hence $T$ is uniquely determined on $V$. $\blacksquare$

This theorem above is very important. It allows us to define any linear map solely by the values it take on a basis.