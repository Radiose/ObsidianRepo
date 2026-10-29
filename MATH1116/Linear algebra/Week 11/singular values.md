# Lemma 
Let $T \in L(V,W)$
Then 
i) $T^*T$ is a [[positive operator]] on $V$
ii) $\ker(T^*T)=\ker(T)$
iii) $range(T^*T)=range(T^*)$
iv) $\operatorname{rank}(T^*T)= \operatorname{rank}(T^*)=\operatorname{rank}(T)$
### Proof 
#### i)
The proof is identical to [[positive operator#iv) $ implies$ i)|this]]
#### ii)
$\subset$
Let $\mathbf{v}\in \ker(T)$, $T^*(T(\mathbf{v}))=T(\mathbf{0})=\mathbf{0}$
$\supset$
$\mathbf{v}\in \ker(T^*T)$, then $T^*(T(\mathbf{v}))=\mathbf{0}$
$\implies \langle T^*T\mathbf{v},\mathbf{v} \rangle=\mathbf{0}$ (via [[inner product space]] axiom 1)
$\implies \langle T\mathbf{v},T\mathbf{v} \rangle=\mathbf{0}$
$\implies T\mathbf{v}=\mathbf{0}$

#### iii) 
$\subseteq$
Let $\mathbf{v}\in range(T^*T)$
$\implies \mathbf{v}=T^*T \mathbf{w}$ for some $\mathbf{w}$
$\implies$ $\mathbf{v}\in range(T^*)$
$\supseteq$
$range(T^*)=\ker(T)^\perp$ (via [[adjoint linear map#Theorem 3 (adjoints swap Ker, Range using perp)|this]])
$=\ker(T^*T)^\perp=range(T^*T)$
#### iv)
exercise

# Definition 
Given $T:V\to W$, we know that the eigenvalues of $T^*T$ are non negative and real via [[positive operator#Theorem|this theorem]].
Therefore, each admits a square root. We list the eigenvalues $s_{1}^2,\dots,s_{\dim(V)}^2$ in non increasing order, and their square roots $s_{1},,\dots,s_{\dim(V)}$ are called the [[singular values]].
