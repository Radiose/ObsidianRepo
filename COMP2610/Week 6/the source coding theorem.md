# Informally 
If you want to uniformly code large [[sequence]]s of outcomes, with any degree of reliability from a random source:
The average number of bits per outcome you need is roughly equal to the [[entropy (information theory)|entropy]] of that source.


# Formally 
Let $X$ be an [[ensemble]] with entropy $H=H(X)$ bits.  Then, $$\forall \epsilon>0, \quad \forall 0 <\delta <1 \quad \exists N_{0} \in\mathbb{N}\quad\forall N>N_{0} \left| \frac{1}{N}H_{\delta}(X^N)-H \right|<\epsilon$$
 Where $H_{\delta}(X^N)$ is the essential bit content. 
 So basically, no matter what reliability $1-\delta$ and tolerance $\epsilon$ you choose, there will always be a long enough sequence so that essential bit content will be tolerantly close to the entropy. 

### Interpretation
If you want to [[source code|uniformly code]] blocks of $N$ symbols, drawn identically and independently, then if you use more than $NH(X)$ bits per block, you can do so with almost no loss of information.

If you use less than $NH(X)$ bits per block, you will almost certainly lose information 


The basis of this is ![[Pasted image 20260902162257.png]]


Above, we can see that the essential bit content of extended ensembles become more and more  predictable.  


# The Source Coding Theorem — Formal Proof

## Statement

**Theorem.** Let $X$ be an ensemble with entropy $H = H(X)$ bits. Given $\epsilon > 0$ and $0 < \delta < 1$, there exists a positive integer $N_0$ such that for all $N > N_0$, $$\left| \frac{1}{N} H_\delta\left(X^N\right) - H \right| < \epsilon.$$

## Definitions used in the proof

**Typical set.** For "closeness" $\beta > 0$, the typical set $T_{N\beta}$ for $X^N$ is $$T_{N\beta} := \{ \mathbf{x} : \left| -\frac{1}{N} \log_2 P(\mathbf{x}) - H(X) \right| < \beta \}$$


**Essential bit content.** For $\delta \geq 0$, let $S_\delta$ be the smallest subset of $\mathcal{A}_{X^N}$ such that $P(\mathbf{x} \in S_\delta) \geq 1-\delta$. Then $$H_\delta\left(X^N\right) = \log_2 |S_\delta|.$$

**Key bound on $T_{N\beta}$.** Rearranging the typical-set definition gives, for every $\mathbf{x} \in T_{N\beta}$, $$2^{-N(H+\beta)} < P(\mathbf{x}) < 2^{-N(H-\beta)}. \tag{1}$$

**AEP.** By the (weak) Law of [[law of large numbers]] applied to $h(X) = -\log_2 P(X)$, for any $\beta > 0$, $$P(\mathbf{x} \in T_{N\beta}) \to 1 \quad \text{as } N \to \infty. \tag{2}$$

## Proof strategy

- **Part 1:** $\dfrac{1}{N} H_\delta\left(X^N\right) < H + \epsilon$
- **Part 2:** $\dfrac{1}{N} H_\delta\left(X^N\right) > H - \epsilon$

---

## Part 1 — Upper bound

**Goal.** For $\epsilon > 0$ and $\delta > 0$, find $N$ large enough that $\frac{1}{N}H_\delta(X^N) < H(X) + \epsilon$.

From the counting consequence of $(1)$: since every $\mathbf{x} \in T_{N\beta}$ has $P(\mathbf{x}) > 2^{-N(H+\beta)}$, and the total probability of $T_{N\beta}$ cannot exceed 1, $$|T_{N\beta}| \cdot 2^{-N(H+\beta)} < 1 \implies |T_{N\beta}| \leq 2^{N(H(X)+\beta)}. \tag{3}$$

By the AEP $(2)$, for any $\delta > 0$ we can always find $N$ large enough that $$P(\mathbf{x} \in T_{N\beta}) \geq 1-\delta.$$

Recall $S_\delta$ is defined as the **smallest** subset achieving coverage $\geq 1-\delta$. Since $T_{N\beta}$ is _some_ subset achieving that coverage, it follows that $$|S_\delta| \leq |T_{N\beta}|.$$

Combining with $(3)$: $$|S_\delta| \leq |T_{N\beta}| \leq 2^{N(H(X)+\beta)}$$ $$\log_2 |S_\delta| \leq \log_2 |T_{N\beta}| \leq N(H(X)+\beta)$$ $$H_\delta\left(X^N\right) \leq N(H(X)+\beta).$$

Setting $\beta = \epsilon$ and dividing through by $N$ gives $$\frac{1}{N} H_\delta\left(X^N\right) \leq H(X) + \epsilon. \qquad \blacksquare \text{ (Part 1)}$$

---

## Part 2 — Lower bound

**Goal.** For $\epsilon > 0$ and $\delta > 0$, find $N$ large enough that $\frac{1}{N}H_\delta(X^N) > H(X) - \epsilon$.

**Proof by contradiction.** Suppose this were _not_ the case — that for every $N$, $$\frac{1}{N} H_\delta\left(X^N\right) \leq H(X) - \epsilon \iff |S_\delta| \leq 2^{N(H(X)-\epsilon)}. \tag{4}$$

Decompose the probability of $S_\delta$ by splitting on membership in $T_{N\beta}$: $$P(\mathbf{x} \in S_\delta) = P\left(\mathbf{x} \in S_\delta \cap T_{N\beta}\right) + P\left(\mathbf{x} \in S_\delta \cap \overline{T_{N\beta}}\right).$$

Bound each term:

- Every $\mathbf{x} \in T_{N\beta}$ satisfies $P(\mathbf{x}) \leq 2^{-N(H-\beta)}$ by $(1)$, so $$P\left(\mathbf{x} \in S_\delta \cap T_{N\beta}\right) \leq |S_\delta| \cdot 2^{-N(H-\beta)}.$$
- Since $S_\delta \cap \overline{T_{N\beta}} \subseteq \overline{T_{N\beta}}$, $$P\left(\mathbf{x} \in S_\delta \cap \overline{T_{N\beta}}\right) \leq P\left(\mathbf{x} \notin T_{N\beta}\right).$$

So: $$P(\mathbf{x} \in S_\delta) \leq |S_\delta| \cdot 2^{-N(H-\beta)} + P\left(\mathbf{x} \notin T_{N\beta}\right).$$

Substitute the contradiction hypothesis $(4)$, taking $\beta = \epsilon$: $$P(\mathbf{x} \in S_\delta) \leq 2^{N(H-\epsilon)} \cdot 2^{-N(H-\epsilon)} + P\left(\mathbf{x} \notin T_{N\beta}\right) = 2^{-N\epsilon}\cdot 2^{N(H-\epsilon)}\cdot 2^{-N(H-\epsilon)}$$

which simplifies to

$$P(\mathbf{x} \in S_\delta) \leq 2^{-N\epsilon} + P\left(\mathbf{x} \notin T_{N\beta}\right).$$

As $N \to \infty$: the first term $2^{-N\epsilon} \to 0$, and by the AEP $(2)$, $P(\mathbf{x} \notin T_{N\beta}) \to 0$. So $$P(\mathbf{x} \in S_\delta) \to 0 \quad \text{as } N \to \infty.$$

But by the **definition** of $S_\delta$, $P(\mathbf{x} \in S_\delta) \geq 1-\delta$ for _every_ $N$ — a fixed positive constant, not something that can shrink to 0.

**Contradiction.** Hence the assumption $(4)$ fails for $N$ large enough, giving $$\frac{1}{N} H_\delta\left(X^N\right) > H(X) - \epsilon. \qquad \blacksquare \text{ (Part 2)}$$

---

## Conclusion

Combining Parts 1 and 2: for any $\epsilon > 0$ and $0 < \delta < 1$, there exists $N_0$ such that for all $N > N_0$, $$H(X) - \epsilon < \frac{1}{N} H_\delta\left(X^N\right) < H(X) + \epsilon \iff \left| \frac{1}{N} H_\delta\left(X^N\right) - H(X) \right| < \epsilon. \qquad \blacksquare$$

## Proof idea, in one line

As $N$ increases: $T_{N\beta}$ has $\approx 2^{NH(X)}$ roughly-equiprobable elements, almost all probability mass lies in $T_{N\beta}$ (via the ), and $S_\delta$ increasingly coincides with $T_{N\beta}$ — so $\log_2 |S_\delta| \sim NH(X)$.