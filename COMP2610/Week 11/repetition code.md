# Background
[[the noisy channel coding theorem]] states that if the probability of some bit error is acceptable, then $(N,K)$ codes exist, with corresponding rates $\frac{K}{N}\leq R(P_{b})= \frac{C}{1-H_{2}(p_{b})}$

# Definition 
A repetition code is the simplest type of linear code. 
We add redundancy by repeating every bit of the message some $n \in \mathbb{N}$ number of times. 

On a binary [[symmetric channel]] with flip probability $f$, the receiver sees $$\mathbf{r}=\mathbf{t}+\eta$$where $\eta$ is some noise vector. 
We define it by $p(\eta_{i}=1)=f$

#### Example 
We set $\eta$ to be some value, and the resulting message $\mathbf{r}$
![[Pasted image 20261113162425.png]]

Note that importantly, we cannot replicate elements of $\eta$ like those of $\mathbf{t}$. It acts independently on all element in a triple. 




# Beyond repetition codes 
![[Hamming code]]