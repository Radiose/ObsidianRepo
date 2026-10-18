
# Overall goal 
![[Pasted image 20261018154134.png]]
somewhat to recreate this. What we have been working on, with [[the source coding theorem]], entropy as a lower bound etc is compression. 

# The fundamental problem of communication 

According to Claude Shannon, there is a fundamental problem is that of reproducing, at one point, either exactly or approximately a message selected at another point. 


# Encoder/Decoder pairs 
Suppose we have some set $\mathcal{S}=\{ 1,2\dots,S \}$ of possible messages. 
The sender, and receiver agree on what these are. 
As an example, use codewords created by [[Huffman coding]] on some ensemble. 

When we communicate, the sender must encode messages into some input alphabet $\mathcal{X}$
The receiver then receives some (possibly corrupt) element from some output alphabet $\mathcal{Y}$
The bits the sender sends, may or may not be the bits that the receiver receives. 

Formally, the encoder is denoted $enc:\mathcal{S}\to \mathcal{X}^N$, and $dec:\mathcal{Y}^N \to \mathcal{S}$

In some sense, source coding is already encoding a message, but we often need to add something in to our code for noise tolerance. 

An $N>1$ is representative of multiple uses of a channel.


![[Discrete channel]]

# Inferring probability 
Suppose we know $p(x)$, and given a particular output $y$ received over a channel $Q$, how likely was the input $x \in \mathcal{X}$ transmitted?
This is the **prime** use case for [[Bayes theorem|bayesian inference]].

Suppose $P(x=0) = P(x=1) = 0.5$. What are the probability that $x = 0$ was transmitted over a [[Discrete channel#The binary symmetric channel|binary symmetric channel]] $Q$ with $f = 0.1$ given that a $y = 0$ was received?

$$
P(x=0 \mid y=0) = \frac{0.9 \times 0.5}{0.9 \times 0.5 + 0.1 \times 0.5} = 0.9
$$

Similarly, $P(x=1 \mid y=1) = 0.9$.

What if $P(x=0) = 0.01$?

$$
P(x=0 \mid y=0) = \frac{0.9 \times 0.01}{0.9 \times 0.01 + 0.1 \times 0.99} \approx 0.0833.
$$
