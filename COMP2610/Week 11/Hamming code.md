We have an overarching goal of communicating over noisy channels. In particular, to be able to communicate with small probability of error, and high rate.
Our current concept of repetition codes introduce redundancy on a per bit basis.
Improving on this can be done via introducing redundancy to blocks of data instead. 

We do this via hamming codes. 

# The (7,4) Hamming code 
This hamming code is based upon the $K=4,N=7$ $(N,K)$ [[block code]]. So it codes length 4 blocks


We demonstrate this via coding the sequence $1\ 0\ 0\ 0$


![[Pasted image 20261113170622.png|428]]
We write the source code bits into the arrangement shown above.
So we get:
![[Pasted image 20261113170604.png|437]]

Then, our parity check bits are the bits that we set $t_{5},t_{6},t_{7}$ in order to ensure EVEN quantities of  $1$ bits inside each circle.

 
![[Pasted image 20261113171116.png|395]]

 ![[Pasted image 20261113171441.png|298]]
This gives us $1,0,1$ as our final sequence of bits we add to our block 

Algebraically, we have set $t_{i}=s_{i}$ for $i=1,..,4$
So, $t_{5}=s_{1} \oplus s_{2} \oplus s_{3}$
$t_{6}=s_{2} \oplus s_{3} \oplus s_{4}$
$t_{7}=s_{1} \oplus s_{3} \oplus s_{4}$
this is more apparent when you view the image above. 


# Matrix form 
Our vector $\mathbf{t}$ is equal to $G^T \mathbf{s}$ with $G^T= \begin{bmatrix}I_{4} \\ P\end{bmatrix}=\begin{bmatrix}1  &   0 & 0 & 0 \\  0 & 1 & 0 & 0 \\  0 & 0 & 1 & 0 \\  0 & 0 & 0 & 1 \\  1 & 1 & 1 & 0 \\  0 & 1 & 1 & 1 \\  1 & 0 & 1 & 1\end{bmatrix}$ and $\mathbf{s}= \begin{bmatrix}s_{1}  \\  s_{2} \\  s_{3}  \\  s_{4}\end{bmatrix}$(note that $I_{4}$ is the identity matrix) 
We call $G$ the **generator matrix**.

Each unique sentence that we can generate is called a codeword. For a $(7,4)$ hamming code we have a total of $16$ codewords. 

We can write $G^T= \begin{bmatrix}G_{1}  & G_{2}  & G_{3}  &  G_{4}\end{bmatrix}$ and from there, we can get a transmitted message as
$t=s_{1}G_{1}+\dots+s_{4}G_{4}$ 


# Decoding hamming codes 
The idea with decoding a hamming code is to just try to find the bit that will make the modulus arithmetic work. 

# Syndrome decoding 
![[syndrome decoding]]


# Decoding with multiple errors 
The way is identical to decoding with singular errors, where we draw the circles and try to unflip whatever appears to be flipped. 

![[Pasted image 20261113184146.png]]

Observe here that it appears that we have a flipped 0 on the right hand side, when in reality we have flipped bits marked with '$^*$'
Flipping it will then give us $3$ errors, but not that only $2$ of them affect the actual message. 



# Error probabilities
Recall that block error is $p_{B}=p(\hat{\mathbf{s}}\not= \mathbf{s})$

Our bit error is $p_{b}=\frac{1}{K}\sum_{k=1}^K p(\hat{\mathbf{s}}_{k}\not= \mathbf{s}_{k})$
And our rate is $\frac{4}{7}$

Block error occurs when $2$ or more bits in the block of $7$ are flipped (impossible to decode properly, as there will always be chance that its not right).

We approximate $p_{B}$ to the leading term, with $p_{B}=\sum_{n=2}^7 \begin{pmatrix}7 \\  \end{pmatrix}f^m(1-f)^{7-m}$ (via the [[binomial distribution]]).
So via the approximation, we end up with $\begin{pmatrix}7  \\   2\end{pmatrix}f^2=21f^2$


Approximating bit error is similar. In the [[Hamming code#Decoding with multiple errors|decoding with multiple errors]] section, we see that $2$ corruptions induce $3$ incorrect bits. 
$\implies p(\mathbf{\hat{s_{i}}}\not=\mathbf{s}_{i}) \approx \frac{3}{7} p_{B}$ for $i=1,..,7$
and $\frac{3}{7}p_{B}=9f^2$
