


$\mathbb{P}(max_{h \in \mathcal{H}}E_{out}(h)-E_{in}(h)\epsilon)8(N+1)^v e^{-N\epsilon^2/32}$
Basically, there is some guarantee that we are able to shrink the [[generalisation gap]].

SO, $E_{out}(h)\leq E_{in}(h)+\sqrt{ \frac{32}{N}\left[ v\log(N+1)+\log \frac{8}{\delta} \right] }$
With the term on the right being our complexity penalty.
Properties:
Fixed $v$, $penalty \xrightarrow[N \to \infty]{}0$
Fixed $N$, penalty grows with $v$. 


Finding the best hypothesis:
Let $h^*\in arg_{h\in \mathcal{H}}E_{out}(h)$ be the best hypothesis in $\mathcal{H}$. The best we could do inside $\mathcal{H}$, even with infinite data. It is unknown because $P$ is. 

- The quality of *learning* in $\mathcal{H}$ is how close $\hat{h}_N$ is to $h^\star$, the **estimation error**

$$
\Delta_{\text{est}} := E_{\text{out}}(\hat{h}_N) - E_{\text{out}}(h^\star) \geq 0
$$

> [!theorem]
> For ERM with the binary loss, if $d_{\text{VC}}(\mathcal{H}) = v < \infty$,
>
> $$
> \mathbb{P}\Big(E_{\text{out}}(\hat{h}_N) - E_{\text{out}}(h^\star) > \epsilon\Big) \leq 8(N+1)^v e^{-N\epsilon^2/128} \xrightarrow[N \to \infty]{} 0.
> $$
>
> *Reference: Devroye, Györfi & Lugosi (1996), A Probabilistic Theory of Pattern Recognition, Chapter 12.*

- Why it follows: if every $h$ has $|E_{\text{out}} - E_{\text{in}}| \leq \epsilon/2$, then
$$
E_{\text{out}}(\hat{h}_N) \leq E_{\text{in}}(\hat{h}_N) + \frac{\epsilon}{2} \leq E_{\text{in}}(h^\star) + \frac{\epsilon}{2} \leq E_{\text{out}}(h^\star) + \epsilon,
$$
using that $\hat{h}_N$ minimises $E_{\text{in}}$ in the middle step


So basically, the essential part is that as $\lim_{ N \to \infty }$, the error shrinks to $0$.