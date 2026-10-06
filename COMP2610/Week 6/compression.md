# Motivation 

"**cn y rd ths mssg?**"
the above sentence demonstrates the *redundancy* in English text. 
Relating to [[information]], there is a very high chance that 'u' will follow 'q'
Compression will aim to exploit differences in relativistic probability between symbols or blocks of symbols.

# Definition 
Data compression is the process of replacing a message with a smaller message that can be reliably converted back to the original.

The main question is about quantifying this reliability. 

The goal is the send a smaller message on average when outcomes are from a fixed, known but uncertain source. 


# Goal of compression 
Mathematically, we have a goal of compression, being to minimise the [[expected code length]].
In particular, we an relate the [[expected code length]] to the [[relative entropy]] $\mathbf{p,q}$:

### Definition 
Given an [[ensemble]] $X$ with probabilities $\mathbf{p}$, and [[prefix code]] $C$ with codeword length probabilities $\mathbf{q}$, and normalisation $z$, $$L(C,X)=H(X)+D_{KL}(\mathbf{p}||\mathbf{q})+\log_{2} \frac{1}{z}$$with equality only when $\ell_{i}=\log_{2} \frac{1}{p_{i}}$.
We have that $L(C,X)$ is minimal and equal to the entropy $H(X)$ if we can choose code lengths such that $D_{KL}(\mathbf{p}||\mathbf{q})=0$ and $\log_{2} \frac{1}{z}{0}$ 