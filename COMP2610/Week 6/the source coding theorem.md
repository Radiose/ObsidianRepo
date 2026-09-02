# Informally 
If you want to uniformly code large [[sequence]]s of outcomes, with any degree of reliability from a random source:
The average number of bits per outcome you need is roughly equal to the [[entropy (information theory)|entropy]] of that source.


# Formally 
Let $X$ be an [[ensemble]] with entropy $H=H(X)$ bits.  Then, $$\forall \epsilon>0, \quad \forall 0 <\delta <1 \quad \exists N_{0} \in\mathbb{N}\quad\forall n>N_{0} \left| \frac{1}{n}H_{\delta}(X^n)-H \right|<\epsilon$$
 Where $H_{\delta}(X^N)$ is the essential bit content. 
 So basically, no matter what reliability $1-\delta$ and tolerance $\epsilon$ you choose, there will always be a long enough sequence so that essential bit content will be tolerantly close to the entropy. 
