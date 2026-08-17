---
{}
---
Suppose $V$ and $W$ are [[vector space]]s with $V$ [[finite dimensional]], and fix $T \in \mathcal{L}(V,W)$. Then, $Range(T)$ is finite dimensional, and $dim(V)=dim(Ker(T))+dim(Range(T))$


### Proof 

Let $\mathbf{u}_1, \ldots, \mathbf{u}_m$ be a basis of $\operatorname{Ker} T$; thus $\dim \operatorname{Ker} T = m$. By Theorem 2.8, the linearly independent set $\{\mathbf{u}_1, \ldots, \mathbf{u}_m\}$ can be extended to a basis

$$\{\mathbf{u}_1, \ldots, \mathbf{u}_m, \mathbf{v}_1, \ldots, \mathbf{v}_n\}$$

of $V$. Thus $\dim V = m + n$. To complete the proof, we only need to show that $\operatorname{Range} T$ is finite-dimensional and $\dim \operatorname{Range} T = n$. We will do this by proving that $\{T(\mathbf{v}_1), \ldots, T(\mathbf{v}_n)\}$ is a basis of $\operatorname{Range} T$.





### Span
Let $v \in V$. Because $\{\mathbf{u}_1, \ldots, \mathbf{u}_m, \mathbf{v}_1, \ldots, \mathbf{v}_n\}$ spans $V$, we can write

$$\mathbf{v} = a_1\mathbf{u}_1 + \cdots + a_m\mathbf{u}_m + b_1\mathbf{v}_1 + \cdots + b_n\mathbf{v}_n,$$

where the $a$'s and $b$'s are in $\mathbb{F}$. Applying $T$ to both sides of this equation, we get

$$T(\mathbf{v}) = b_1 T(\mathbf{v}_1) + \cdots + b_n T(\mathbf{v}_n),$$

where we used the assumption that $T(\mathbf{u}_j) = \mathbf{0}$ for each $\mathbf{u}_j$, since $\mathbf{u}_j$ is in $\operatorname{Ker} T$. The last equation implies that $\{T(\mathbf{v}_1), \ldots, T(\mathbf{v}_n)\}$ spans $\operatorname{Range} T$. In particular, $\operatorname{Range} T$ is finite-dimensional.


### Independence
To show $\{T(\mathbf{v}_1), \ldots, T(\mathbf{v}_n)\}$ is linearly independent, suppose $c_1, \ldots, c_n \in \mathbf{F}$ and

$$c_1 T(\mathbf{v}_1) + \cdots + c_n T(\mathbf{v}_n) = \mathbf{0}.$$

Then, by linearity of $T$,

$$T(c_1\mathbf{v}_1 + \cdots + c_n\mathbf{v}_n) = \mathbf{0}.$$

Hence

$$c_1\mathbf{v}_1 + \cdots + c_n\mathbf{v}_n \in \operatorname{Ker} T.$$

Because $\mathbf{u}_1, \ldots, \mathbf{u}_m$ spans $\operatorname{Ker} T$, we can write

$$c_1\mathbf{v}_1 + \cdots + c_n\mathbf{v}_n = d_1\mathbf{u}_1 + \cdots + d_m\mathbf{u}_m,$$

where the $d$'s are in $\mathbf{F}$. This equation implies that all the $c$'s (and $d$'s) are $0$, because $\{\mathbf{u}_1, \ldots, \mathbf{u}_m, \mathbf{v}_1, \ldots, \mathbf{v}_n\}$ is linearly independent. Thus $\{T(\mathbf{v}_1), \ldots, T(\mathbf{v}_n)\}$ is linearly independent and hence is a basis of $\operatorname{Range} T$, as desired. $\blacksquare$

