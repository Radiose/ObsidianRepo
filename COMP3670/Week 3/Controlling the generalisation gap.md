# Finite data 
Thought experiment: Can you determine the number  of green marbles in a bag of red and green ones purely by sampling the proportion of green marbles that you draw? 
No. But, it would be very unlikely. 
Fix a hypothesis $h$. colour an example red if $h$ gets it wrong.  
![[Hoeffdings inequality]]
Applying this to a singular hypothesis:
$\mathbb{P}(|E_{out}(h)-E_{in}(h)|>\epsilon)\leq 2e^{-2N\epsilon^2}$

The usual way we view the bound:
$E_{out }(h)\leq E_{in}(h)+\sqrt{ \frac{1}{2N}\log \frac{2}{\delta} }$
The penalty (right sqrt) decreases like $\frac{1}{\sqrt{ N }}$. To halve the error bar, we need four times as much data. 

Importantly, $h$ had to be fixed, before looking at the sample. 
What this is was verification, not learning, in which $\hat{h}$ was chosen **using** the sample. 
[[Empirical risk minimisation]] will report the hypothesis with the best in sample record. Whatever minimises has some bias. 

The fix for this, is the [[union bound]]. We cover all hypothesis in the [[hypothesis set]] $\mathcal{H}$.


- Let $\mathcal{H} = \{h_1, \dots, h_M\}$ be **finite**. The event "*some hypothesis has a large gap*" is a **union** of $M$ events, so the union bound of Lecture 2 applies:

$$
\begin{aligned}
\mathbb{P}\left(\max_{h \in \mathcal{H}} |E_{\text{out}}(h) - E_{\text{in}}(h)| > \epsilon\right) &= \mathbb{P}\left(\bigcup_{j=1}^{M} \left\{|E_{\text{out}}(h_j) - E_{\text{in}}(h_j)| > \epsilon\right\}\right) \\
&\leq \sum_{j=1}^{M} \mathbb{P}\left(|E_{\text{out}}(h_j) - E_{\text{in}}(h_j)| > \epsilon\right) \\
&\leq \sum_{j=1}^{M} 2e^{-2N\epsilon^2} = 2M e^{-2N\epsilon^2}
\end{aligned}
$$

- Each inequality used one fact only: the union bound for the first, [[Hoeffdings inequality]] for the second.

Its incredibly important to note here that this sort of bounding of the [[generalisation gap]] is only possible here because we have finite data.