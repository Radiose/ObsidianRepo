If $\mathcal{A}$ is a finite set, then $A^N$ is the set of all strings of length $N$.
$\mathcal{A}^{+}=\bigcup_{N}\mathcal{A^N}$ is the set of all finite strings.

Let $X$ be an [[ensemble]] with $\mathcal{A}_{X}=\{ a_{1},\dots,a_{n} \}$.
A function $c: \mathcal{A}_{X}\to \{ 0,1 \}^+$ is a code for $X$.

The binary string $c(x)$ is the codeword for $x \in \mathcal{A}_{X}$
The length of the codeword for $x$ is denoted $\ell(x)$
Note $\ell_{i}=\ell(c_{i})$ for $i=1,\dots,l$
The extension of $c$ assigns codewords to any [[sequence]] $x_{1}x_{2},\dots,x_{N}$ from $\mathcal{A}^+$ by $c(x_{1}x_{2},\dots,x_{n})=c(x_{1})\dots c(x_{n})$
